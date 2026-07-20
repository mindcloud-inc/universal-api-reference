# Send Messages with Sakari SMS

Sends text messages through Sakari SMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:accountId/messages`
- **Base URL:** `https://api.sakari.io`
- **Official documentation:** [Send Messages](https://developer.sakari.io/api-reference/messages/send-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversations[]` | body | `array<string>` | no | List of conversation ids to send messages to |
| `contacts[]` | body | `array<object>` | no | — |
| `contacts.contacts[].id` | body | `string` | no | — |
| `contacts.contacts[].email` | body | `string` | no | — |
| `contacts.contacts[].firstName` | body | `string` | no | — |
| `contacts.contacts[].lastName` | body | `string` | no | — |
| `contacts.contacts[].mobile` | body | `object` | no | — |
| `contacts.contacts[].mobile.country` | body | `string` | no | — |
| `contacts.contacts[].mobile.number` | body | `string` | no | — |
| `contacts.contacts[].mobile.verified` | body | `date` | no | — |
| `contacts.contacts[].mobile.valid` | body | `boolean` | no | — |
| `contacts.contacts[].mobile.lineType` | body | `string` | no | — |
| `contacts.contacts[].lists[]` | body | `array<object>` | no | — |
| `contacts.contacts[].lists.lists[].id` | body | `string` | no | — |
| `contacts.contacts[].lists.lists[].name` | body | `string` | no | — |
| `contacts.contacts[].lists.lists[].source` | body | `object` | no | — |
| `contacts.contacts[].lists.lists[].keyword` | body | `string` | no | — |
| `contacts.contacts[].lists.lists[].doubleOptIn` | body | `object` | no | — |
| `contacts.contacts[].lists.lists[].filter` | body | `object` | no | — |
| `contacts.contacts[].lists.lists[].optInConfirmation` | body | `string` | no | — |
| `contacts.contacts[].lists.lists[].optIn` | body | `date` | no | — |
| `contacts.contacts[].lists.lists[].optOut` | body | `date` | no | — |
| `contacts.contacts[].attributes` | body | `object` | no | — |
| `contacts.contacts[].optIn` | body | `date` | no | — |
| `contacts.contacts[].blocked` | body | `date` | no | — |
| `contacts.contacts[].activecampaign` | body | `object` | no | — |
| `contacts.contacts[].activecampaign.id` | body | `number` | no | — |
| `contacts.contacts[].hubspot` | body | `object` | no | — |
| `contacts.contacts[].hubspot.id` | body | `number` | no | — |
| `contacts.contacts[].pipedrive` | body | `object` | no | — |
| `contacts.contacts[].pipedrive.id` | body | `number` | no | — |
| `contacts.contacts[].valid` | body | `boolean` | no | — |
| `contacts.contacts[].error` | body | `object` | no | — |
| `contacts.contacts[].error.code` | body | `string` | no | — |
| `contacts.contacts[].error.description` | body | `string` | no | — |
| `contacts.contacts[].created` | body | `object` | no | — |
| `contacts.contacts[].created.at` | body | `date` | no | — |
| `contacts.contacts[].created.by` | body | `object` | no | — |
| `contacts.contacts[].updated` | body | `object` | no | — |
| `contacts.contacts[].updated.at` | body | `date` | no | — |
| `contacts.contacts[].updated.by` | body | `object` | no | — |
| `filters` | body | `object` | no | — |
| `filters.tags[]` | body | `array<string>` | no | — |
| `filters.attributes[]` | body | `array<object>` | no | — |
| `phoneNumberFilter` | body | `object` | no | — |
| `phoneNumberFilter.group` | body | `object` | no | — |
| `phoneNumberFilter.group.id` | body | `string` | no | — |
| `template` | body | `string` | no | — |
| `type` | body | `string` | no | — |
| `media[]` | body | `array<object>` | no | List of media objects to attach to message |
| `media.media[].url` | body | `string` | no | — |
