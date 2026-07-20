# Start Lead Mail Sequence with DealMachine

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/leads/:lead_id/start-mail-sequence`
- **Base URL:** `https://api.dealmachine.com`
- **Official documentation:** [Start Lead Mail Sequence](https://docs.dealmachine.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `number` | yes | The DealMachine lead ID. |
| `mailer_campaign_id` | body | `string` | no | Optional DealMachine mail sequence ID. If omitted, the default mail sequence is used. |
