# Update Recipient with Hyperstack Certificates

## Endpoint

- **Method:** `POST`
- **Path:** `/recipients/update`
- **Base URL:** `https://api.thehyperstack.com/v1`
- **Official documentation:** [Update Recipient](https://thehyperstack.com/docs/api-guide/update-recipient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_attributes` | body | `object` | yes | Custom recipient fields to update. Keys must be prefixed with custom_. |
| `email` | body | `string` | yes | The email address of the recipient to update. |
