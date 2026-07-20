# List Project Billing Fields with Deepgram

Retrieves project billing fields from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/billing/fields`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [List Project Billing Fields](https://developers.deepgram.com/reference/manage/billing/fields/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Deepgram project identifier. |
| `start` | query | `string` | no | Start date for the requested billing-field range in YYYY-MM-DD format. |
| `end` | query | `string` | no | End date for the requested billing-field range in YYYY-MM-DD format. |
