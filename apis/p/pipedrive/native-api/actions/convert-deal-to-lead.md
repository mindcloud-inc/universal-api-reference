# Convert Deal To Lead with Pipedrive

Converts a deal to a lead in Pipedrive.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/deals/:id/convert/lead`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Convert Deal To Lead](https://developers.pipedrive.com/docs/api/v1/Deals#convertDealToLead)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/plain` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique ID of the deal to convert. |
