# End Lead Mail Sequence with DealMachine

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/leads/:lead_id/end-mail-sequence`
- **Base URL:** `https://api.dealmachine.com`
- **Official documentation:** [End Lead Mail Sequence](https://docs.dealmachine.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `number` | yes | The DealMachine lead ID. |
| `mailer_campaign_id` | body | `string` | yes | The DealMachine mail sequence ID to end for the lead. |
