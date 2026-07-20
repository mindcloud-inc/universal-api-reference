# Organization Enrichment with Apollo

Retrieves enriched data for an organization from Apollo.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/organizations/enrich`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Organization Enrichment](https://docs.apollo.io/reference/organization-enrichment)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | The domain of the company that you want to enrich. Do not include `www.`, the `@` symbol, or similar. Example: `apollo.io` or `microsoft.com` |
