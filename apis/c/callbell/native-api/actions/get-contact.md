# Get Contact with Callbell

Retrieves a specific contact from Callbell.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:uuid`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [Get Contact](https://docs.callbell.eu/api/reference/contacts_api/get_contact/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_field_types` | query | `boolean` | no | Include custom field metadata in the response. |
| `uuid` | path | `string` | yes | Unique identifier of the contact. |
