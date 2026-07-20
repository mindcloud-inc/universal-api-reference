# Get Project Billing Breakdown with Deepgram

Retrieves a project billing breakdown from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/billing/breakdown`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [Get Project Billing Breakdown](https://developers.deepgram.com/reference/manage/billing/breakdown/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Deepgram project identifier. |
| `start` | query | `string` | no | Start date of the requested billing range in YYYY-MM-DD format. |
| `end` | query | `string` | no | End date of the requested billing range in YYYY-MM-DD format. |
| `accessor` | query | `string` | no | Filter billing breakdown rows by accessor identifier. |
| `deployment` | query | `string` | no | Filter billing breakdown rows by deployment: hosted, beta, or self-hosted. |
| `tag` | query | `string` | no | Filter billing breakdown rows by a specific tag. |
| `line_item` | query | `string` | no | Filter billing breakdown rows by line item, for example streaming::nova-3. |
| `grouping` | query | `string` | no | Grouping dimensions encoded as a JSON-style list string, for example ["deployment","line_item"]. |
