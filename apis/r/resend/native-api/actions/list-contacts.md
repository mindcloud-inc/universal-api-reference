# List Contacts with Resend

Retrieves contacts from Resend.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [List Contacts](https://resend.com/docs/api-reference/contacts/list-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `segment_id` | query | `string` | no | Filter contacts by segment. Only contacts in this segment will be returned. Maximum length: 0. |
