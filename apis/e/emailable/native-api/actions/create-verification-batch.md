# Create Verification Batch with Emailable

Creates an email verification batch in Emailable.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/batch`
- **Base URL:** `https://api.emailable.com`
- **Official documentation:** [Create Verification Batch](https://emailable.com/docs/api/#verify-a-batch-of-emails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails` | body | `string` | yes | One or more email addresses to verify in the batch. Send multiple values as a string separated by `,`. |
| `url` | body | `string` | no | Optional URL that receives the completed batch result via HTTP POST. |
| `retries` | body | `boolean` | no | Leave enabled to retry certain mail-server responses for better accuracy. |
| `response_fields` | body | `string` | no | Optional list of per-email response fields to include in the batch result. Send multiple values as a string separated by `,`. |
