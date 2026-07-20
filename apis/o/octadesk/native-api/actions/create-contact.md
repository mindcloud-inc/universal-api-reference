# Create Contact with Octadesk

Creates a contact in Octadesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Contact](https://developers.octadesk.com/reference/addcontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Customer email. |
| `name` | body | `string` | yes | Customer name. |
