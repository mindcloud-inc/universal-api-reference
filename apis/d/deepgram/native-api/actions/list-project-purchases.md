# List Project Purchases with Deepgram

Retrieves project purchases from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/purchases`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [List Project Purchases](https://developers.deepgram.com/reference/manage/billing/purchases/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Deepgram project identifier. |
| `limit` | query | `number` | no | Number of purchases to return per page. |
