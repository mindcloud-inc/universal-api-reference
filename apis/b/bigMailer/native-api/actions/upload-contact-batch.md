# Upload Contact Batch with BigMailer

Uploads a batch of contacts to create or update asynchronously in a BigMailer brand.

## Endpoint

- **Method:** `POST`
- **Path:** `/brands/:brand_id/contacts/batches`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Upload Contact Batch](https://docs.bigmailer.io/reference/createcontactbatch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand to upload contacts into. |
| `validate` | body | `boolean` | no | Validate contact emails before importing them. |
| `items[]` | body | `array<object>` | yes | Contacts to upload in this batch. |
