# Import Contacts with ActiveTrail

Imports contacts into a group in ActiveTrail.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/Import`
- **Base URL:** `https://webapi.mymarketing.co.il/api`
- **Official documentation:** [Import Contacts](https://webapi.mymarketing.co.il/api/docs/and/Api/POST-api-contacts-Import)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes | Contacts to import. Limited to 1000. |
| `contacts[].anniversary` | body | `date` | no | — |
| `contacts[].birthday` | body | `date` | no | — |
| `contacts[].city` | body | `string` | no | — |
| `contacts[].email` | body | `string` | no | — |
| `contacts[].first_name` | body | `string` | no | — |
| `contacts[].last_name` | body | `string` | no | — |
| `contacts[].phone1` | body | `string` | no | — |
| `contacts[].phone2` | body | `string` | no | — |
| `contacts[].sms` | body | `string` | no | — |
| `group` | body | `number` | yes | Group id. Required. |
| `mailing_list` | body | `number` | no | Mailing list id. Delete it if you don't have mailing lists on your account. |
