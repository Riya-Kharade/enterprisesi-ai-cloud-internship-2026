# Task 3: Integrations & Node Mastery (Module 2)

## Intern Details

-   Name: Riya Sunil Kharade
-   Internship Role: AI & Cloud Research Intern
-   Module: Module 2 -- Integrations & Node Mastery

------------------------------------------------------------------------

## Objective

This module focuses on mastering integrations in n8n by effectively
using the HTTP Request node and built-in SaaS nodes.

The goal is to understand: - How APIs communicate - How authentication
works - How pagination is handled - How to build reliable API-to-API
synchronization workflows - How to implement proper error handling and
retry logic

------------------------------------------------------------------------

## 1. HTTP Request Node (Critical Skill)

The HTTP Request node is one of the most important nodes in n8n. It
allows workflows to interact with external APIs when a dedicated n8n
node is not available.

### Key Capabilities

-   Supports HTTP methods: GET, POST, PUT, PATCH, DELETE
-   Sends and receives JSON data
-   Handles authentication and custom headers
-   Works with REST APIs and web services

### Common Use Cases

-   Fetch data from external systems
-   Send data to third-party applications
-   Integrate custom or internal APIs
-   Replace manual API calls with automation

### Configuration Parameters

-   URL (API endpoint)
-   Method (GET/POST/etc.)
-   Headers (Authorization, Content-Type)
-   Body (JSON payload)
-   Query Parameters (Filtering, pagination)

------------------------------------------------------------------------

## 2. API Pagination and Authentication Patterns

### API Pagination

Many APIs return data in pages instead of sending all records at once.

#### Common Pagination Techniques

-   Page-based (page=1, page=2)
-   Offset-based (offset + limit)
-   Cursor-based (next_cursor, next_token)

#### Implementation in n8n

-   Use Looping with IF and Merge nodes
-   Store page/cursor values in workflow variables
-   Continue execution until no more pages exist

------------------------------------------------------------------------

### Authentication Patterns

APIs require authentication to ensure secure access.

#### Common Types

-   API Key Authentication
-   Bearer Token Authentication
-   OAuth 2.0
-   Basic Authentication

n8n supports credential management to securely store and reuse
authentication details.

------------------------------------------------------------------------

## 3. Working with SaaS Nodes (Slack, Jira, Salesforce, GitHub, etc.)

n8n provides pre-built nodes for popular SaaS platforms.

### Advantages

-   No need to manually handle API endpoints
-   Built-in authentication support
-   Simplified configuration
-   Faster workflow development

### Examples

-   Slack: Send messages and alerts
-   GitHub: Create issues and manage repositories
-   Jira: Create and update tickets
-   Salesforce: Manage CRM records

### Best Practice

-   Use SaaS nodes when available
-   Use HTTP Request node for unsupported or advanced operations

------------------------------------------------------------------------

## 4. Custom Headers, OAuth, and Token Refresh

### Custom Headers

Used to pass additional information: - Authorization tokens - Content
type - API version

Example: Authorization: Bearer `<access_token>`{=html}\
Content-Type: application/json

------------------------------------------------------------------------

### OAuth 2.0 Authentication

OAuth is commonly used by SaaS platforms for secure access.

#### OAuth Flow in n8n

1.  User authorizes application
2.  Access token is generated
3.  Token is stored in credentials
4.  Token is refreshed automatically when expired

### Token Refresh Handling

-   n8n automatically refreshes tokens when configured
-   Prevents workflow failures due to expired tokens

------------------------------------------------------------------------

## 5. Lab 2: Build an API-to-API Sync Workflow

### Objective

Create a workflow that synchronizes data between two different APIs
automatically.

### Workflow Overview

-   Fetch data from Source API
-   Transform data
-   Send data to Destination API
-   Handle errors and retries

### Nodes Used

-   HTTP Request (Source API)
-   Set / Function Node (Data transformation)
-   HTTP Request (Destination API)
-   IF Node (Validation)
-   Error handling workflow

### Steps

1.  Trigger workflow (Manual/Cron)
2.  Fetch records from Source API
3.  Map required fields
4.  Push data to Destination API
5.  Log success or failure

------------------------------------------------------------------------

## 6. Retry Logic and Rate-Limit Handling

### Retry Logic

Ensures reliability when APIs temporarily fail.

#### Implementation

-   Configure "Retry on Fail" in HTTP Request node
-   Set retry count and delay
-   Handle network/time-out errors

------------------------------------------------------------------------

### Rate-Limit Handling

APIs limit the number of requests per minute/hour.

#### Strategies

-   Introduce delays using Wait node
-   Batch requests
-   Respect API rate-limit headers
-   Avoid parallel execution when limits are strict

------------------------------------------------------------------------

## 7. Outcome of This Module

After completing this module, I can:

-   Integrate any REST API using n8n
-   Handle authentication securely
-   Manage pagination efficiently
-   Build robust API-to-API sync workflows
-   Implement retries and handle rate-limits
-   Work confidently with SaaS and custom APIs

------------------------------------------------------------------------

## Conclusion

This module builds a strong foundation in API integrations using n8n.

Mastering these concepts is essential for building scalable, reliable,
and production-ready automation workflows.
