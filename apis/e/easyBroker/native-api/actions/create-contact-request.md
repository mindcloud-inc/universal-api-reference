# Create Contact Request with EasyBroker

Creates or updates a property contact request in EasyBroker.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact_requests`
- **Base URL:** `https://api.easybroker.com/v1`
- **Official documentation:** [Create Contact Request](https://dev.easybroker.com/reference/post_contact-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `property_id` | body | `string` | yes | Property ID that received the contact request. |
| `name` | body | `string` | yes | Lead full name. |
| `email` | body | `string` | no | Lead email address. |
| `phone` | body | `string` | no | Lead phone number. |
| `message` | body | `string` | yes | Lead message. |
| `source` | body | `string` | yes | Contact source label. |
