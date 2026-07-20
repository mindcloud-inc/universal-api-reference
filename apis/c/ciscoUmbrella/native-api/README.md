# Cisco Umbrella: Native API Reference

A consolidated summary of Cisco Umbrella's API configuration, with links to official documentation.

- **Official docs:** https://developer.cisco.com/docs/cloud-security/umbrella-api-getting-started/
- **API base URL:** `https://api.umbrella.com`

## Authentication

### API Key Connection

Cisco Umbrella API key connection. The API key and key secret are exchanged with Cisco's OAuth2 client-credentials token endpoint before API calls.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.umbrella.com/auth/v2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `admin.users:read admin.roles:read admin.organizations:read deployments.networks:read deployments.sites:read deployments.internalnetworks:read deployments.roamingcomputers:read policies.destinationLists:read policies.destinations:read policies.destinations:write investigate.investigate:read investigate.bulk:read reports.aggregations:read reports.appDiscovery:read reports.apiusage:read`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://developer.cisco.com/docs/cloud-security/umbrella-api-authentication/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
