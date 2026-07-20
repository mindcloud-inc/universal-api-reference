# Bulk Organization Enrichment with Apollo

Retrieves enriched data for up to 10 organizations from Apollo.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/organizations/bulk_enrich`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Bulk Organization Enrichment](https://docs.apollo.io/reference/bulk-organization-enrichment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domains[]` | body | `array<string>` | yes | Send multiple values as a array. |
