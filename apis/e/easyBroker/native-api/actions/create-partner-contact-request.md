# Create Partner Contact Request with EasyBroker

Creates a partner contact request in EasyBroker.

## Endpoint

- **Method:** `POST`
- **Path:** `/integration_partners/contact_requests`
- **Base URL:** `https://api.easybroker.com/v1`
- **Official documentation:** [Create Partner Contact Request](https://dev.easybroker.com/reference/post_contact-requests-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Requester email. Required if phone is not present. |
| `message` | body | `string` | yes | Message of the contact request. |
| `name` | body | `string` | no | Requester name. |
| `phone` | body | `string` | no | Requester phone number. Required if email is not present. |
| `property_id` | body | `string` | yes | The EasyBroker property id related to the contact request. |
| `remote_id` | body | `number` | yes | A unique numeric id of the contact request from your website. |
