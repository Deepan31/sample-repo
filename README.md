Act as a Principal Software Architect with deep expertise in AWS, .NET, Next.js, DynamoDB, OpenSearch, distributed systems, and scalable cloud-native applications.

I want to understand the Search module in my project from an architectural perspective, not just the implementation.

Analyze the existing codebase and explain:

1. Overall search architecture
   - How the search request flows from UI to backend.
   - Which services are involved.
   - Where OpenSearch fits in the architecture.
   - Where DynamoDB is used.
   - Whether Redis or in-memory cache is involved.

2. OpenSearch
   - Which indexes are being queried.
   - How indexes are created.
   - How documents are indexed.
   - What document mappings are used.
   - Which fields are searchable.
   - Which fields are filterable.
   - Which fields are sortable.
   - How pagination is implemented.
   - How relevance scoring works.
   - Whether the project uses REST APIs or the OpenSearch .NET client.

3. Search API
   For each endpoint:
   - Request flow
   - Validation
   - Query construction
   - Filters
   - Sorting
   - Pagination
   - Response mapping
   - Performance optimizations

4. DynamoDB
   Explain why DynamoDB is still required if OpenSearch exists.
   Identify:
   - Which APIs query DynamoDB directly.
   - Which APIs query OpenSearch.
   - Which data is considered the source of truth.
   - How synchronization between DynamoDB and OpenSearch happens.

5. Performance
   Explain:
   - Why OpenSearch is used instead of DynamoDB for searching.
   - Which operations are expensive.
   - Which indexes improve performance.
   - Any caching strategy.
   - Potential bottlenecks.
   - Recommendations for improving latency.

6. AWS Architecture
   Explain why each AWS service was chosen:
   - OpenSearch
   - DynamoDB
   - S3
   - EventBridge
   - SNS
   - SQS
   - Lambda
   - CloudWatch
   - X-Ray

7. Code walkthrough
   Starting from the Search API Controller, trace the entire request path:
   Controller
   ↓
   Service
   ↓
   Repository
   ↓
   OpenSearch/DynamoDB
   ↓
   Response

Show the actual classes, interfaces, and methods involved.

8. Architecture review
   Evaluate the implementation as if reviewing a production system.
   Identify:
   - Good design decisions.
   - Violations of SOLID or Clean Architecture.
   - Scalability concerns.
   - Maintainability issues.
   - Performance risks.
   - Security concerns.

9. Learning
   Assume I am the developer responsible for this module.
   Explain every important concept so I understand not only WHAT the code does, but WHY it was designed this way and when this architecture should be chosen in enterprise systems.

Important:
- Base every answer only on the existing codebase.
- Do not assume behavior that is not present in the code.
- If something cannot be determined, explicitly state that.
- Include code references whenever possible.
- Use diagrams or flowcharts where helpful.

For GitHub Copilot Agent

Run this prompt at the solution root after opening the entire workspace. It will traverse controllers, services, repositories, and OpenSearch-related code to produce an architecture explanation tied to your code.

For Amazon Q

The same prompt works well. If the codebase is large, ask it to proceed incrementally:

Start with Step 1 only (Overall Search Architecture). After completing it, wait for my confirmation before moving to Step 2.
