# Generate Authorization Link For A Single Data Source with Windsor.ai

Generates a Windsor.ai authorization link for one data source.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/team/generate-co-user-url/`
- **Base URL:** `https://onboard.windsor.ai`
- **Official documentation:** [Generate Authorization Link For A Single Data Source](https://windsor.ai/api-documentation/#tab-content28)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowed_sources` | query | `string` | yes | Restrict the generated authorization link to one Windsor.ai source ID. |
