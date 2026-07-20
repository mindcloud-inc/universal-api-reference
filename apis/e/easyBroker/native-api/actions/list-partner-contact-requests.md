# List Partner Contact Requests with EasyBroker

Retrieves partner contact requests from EasyBroker.

## Endpoint

- **Method:** `GET`
- **Path:** `/integration_partners/contact_requests`
- **Base URL:** `https://api.easybroker.com/v1`
- **Official documentation:** [List Partner Contact Requests](https://dev.easybroker.com/reference/get_contact-requests-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `happened_after` | query | `string` | no | Contact requests created after the given date. |
| `happened_before` | query | `string` | no | Contact requests created before the given date. |
| `property_id` | query | `string` | no | Retrieve contact requests for one property. |
