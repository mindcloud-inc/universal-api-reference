# List Contacts with Callbell

Retrieves contacts for the current Callbell account.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [List Contacts](https://docs.callbell.eu/api/reference/contacts_api/get_contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_field_types` | query | `boolean` | no | Include custom field metadata in the response. |
| `page` | query | `number` | no | Page number to retrieve. |
| `source` | query | `string` | no | Filter contacts by integration source such as whatsapp. |
| `tags` | query | `string` | no | Comma-separated list of tags to match. |
| `team_uuid` | query | `string` | no | Filter contacts by team UUID. |
