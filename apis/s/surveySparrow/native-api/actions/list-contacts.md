# List Contacts with SurveySparrow

Retrieves all contacts from SurveySparrow.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [List Contacts](https://developers.surveysparrow.com/rest-apis/get-v-3-contacts/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_list_id` | query | `number` | no | Filter contacts by contact list ID. |
| `type` | query | `list` | no | Filter contacts by delivery status. Accepted values: `0`, `1`, `2`. |
| `search` | query | `string` | no | Search all contact properties for a matching value. |
| `contact_type` | query | `list` | no | Filter by contact type. Accepted values: `0`, `1`. |
| `created_date.gte` | query | `date` | no | Return contacts created on or after this date. |
| `created_date.lte` | query | `date` | no | Return contacts created on or before this date. |
