# Create Contact with Sakari SMS

Creates a new contact in Sakari SMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:accountId/contacts`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Create Contact](https://developer.sakari.io/api-reference/contacts/create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | — |
| `firstName` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `mobile` | body | `object` | no | — |
| `mobile.country` | body | `string` | yes | — |
| `mobile.number` | body | `string` | yes | — |
| `mobile.verified` | body | `date` | no | — |
| `mobile.valid` | body | `boolean` | no | — |
| `mobile.lineType` | body | `string` | no | — |
| `lists[]` | body | `array<object>` | no | — |
| `lists.lists[].id` | body | `string` | no | — |
| `lists.lists[].name` | body | `string` | no | — |
| `lists.lists[].source` | body | `object` | no | — |
| `lists.lists[].source.id` | body | `string` | no | — |
| `lists.lists[].source.integration` | body | `string` | no | — |
| `lists.lists[].source.lastSynced` | body | `string` | no | — |
| `lists.lists[].keyword` | body | `string` | no | — |
| `updated.by.subSource` | query | `string<object>` | no | Determines how existing contacts with matching mobile numbers are treated |
