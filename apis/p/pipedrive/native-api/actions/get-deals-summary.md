# Get Deals Summary with Pipedrive

Retrieves deal summary metrics from Pipedrive.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/deals/summary`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Get Deals Summary](https://developers.pipedrive.com/docs/api/v1/Deals#getDealsSummary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter by status: open, won, or lost. |
