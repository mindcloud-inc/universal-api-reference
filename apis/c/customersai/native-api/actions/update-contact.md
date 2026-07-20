# Update Contact with Customers.ai

Updates an existing contact in Customers.ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:recipient_id`
- **Base URL:** `https://api.mobilemonkey.com/public`
- **Official documentation:** [Update Contact](https://customers.ai/help/l/en/article/4xafzjcgyr-update-contact-attributes-via-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipient_id` | path | `string` | yes | Recipient ID or contact ID of the contact to update. |
| `EMAIL` | body | `string` | no | Updated email address for the contact. |
| `ATTRIBUTE_1` | body | `string` | no | Optional sample custom attribute value. |
