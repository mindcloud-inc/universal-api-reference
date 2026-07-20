# Update Contact with Smoove

Updates an existing contact in Smoove by identifier.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/Contacts/:id`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [Update Contact](https://rest.smoove.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `by` | query | `list` | no | Accepted values: `CellPhone`, `ContactId`, `Email`, `ExternalId`. |
| `email` | body | `string` | no | — |
| `externalId` | body | `string` | no | — |
| `firstName` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `cellPhone` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `password` | body | `string` | no | — |
| `dateOfBirth` | body | `date` | no | — |
| `address` | body | `string` | no | — |
| `city` | body | `string` | no | — |
| `country` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `position` | body | `string` | no | — |
| `canReceiveEmails` | body | `boolean` | no | — |
| `canReceiveSmsMessages` | body | `boolean` | no | — |
| `lists_ToSubscribe[]` | body | `array<number>` | no | — |
| `lists_ToUnsubscribe[]` | body | `array<number>` | no | — |
| `customFields` | body | `object` | no | — |
| `options` | body | `object` | no | — |
| `campaignSource` | body | `string` | no | — |
| `restoreIfDeleted` | query | `boolean` | no | — |
| `restoreIfUnsubscribed` | query | `boolean` | no | — |
| `overrideNullableValue` | query | `boolean` | no | — |
