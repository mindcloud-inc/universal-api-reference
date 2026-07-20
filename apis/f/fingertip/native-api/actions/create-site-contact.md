# Create Site Contact with Fingertip

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/site-contacts`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Create Site Contact](https://docs.fingertip.com/openapi-specs/create-site-contact.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Contact email address. |
| `siteId` | body | `string` | yes | Site ID. |
| `firstName` | body | `string` | no | Contact first name. |
| `lastName` | body | `string` | no | Contact last name. |
| `phone` | body | `string` | no | Contact phone number. |
| `notes` | body | `string` | no | Internal notes. |
| `marketingStatus` | body | `string` | no | Optional marketing status. |
