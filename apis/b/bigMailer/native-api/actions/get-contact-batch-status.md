# Get Contact Batch Status with BigMailer

Retrieves the status of a contact batch from a BigMailer brand.

## Endpoint

- **Method:** `GET`
- **Path:** `/brands/:brand_id/contacts/batches/:batch_id`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Get Contact Batch Status](https://docs.bigmailer.io/reference/getcontactbatch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand that owns the contact batch. |
| `batch_id` | path | `string` | yes | ID of the contact batch. |
