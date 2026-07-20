# Create Contact with Syncro

Creates a new contact in Syncro.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [Create Contact](https://api-docs.syncromsp.com/#/Contact/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer_id` | body | `number` | yes |
| `name` | body | `string` | no |
| `address1` | body | `string` | no |
| `address2` | body | `string` | no |
| `city` | body | `string` | no |
| `state` | body | `string` | no |
| `zip` | body | `string` | no |
| `email` | body | `string` | no |
| `phone` | body | `string` | no |
| `mobile` | body | `string` | no |
| `notes` | body | `string` | no |
