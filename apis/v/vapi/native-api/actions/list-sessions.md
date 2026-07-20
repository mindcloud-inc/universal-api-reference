# List Sessions with Vapi

Retrieves a list of sessions from Vapi.

## Endpoint

- **Method:** `GET`
- **Path:** `/session`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [List Sessions](https://docs.vapi.ai/api-reference/sessions/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | This is the unique identifier for the session to filter by. |
| `name` | query | `string` | no | This is the name of the session to filter by. |
| `assistantId` | query | `string` | no | This is the ID of the assistant to filter sessions by. |
| `assistantIdAny` | query | `string` | no | Filter by multiple assistant IDs. Provide as comma-separated values. |
| `squadId` | query | `string` | no | This is the ID of the squad to filter sessions by. |
| `workflowId` | query | `string` | no | This is the ID of the workflow to filter sessions by. |
| `numberE164CheckEnabled` | query | `boolean` | no | This is the flag to toggle the E164 check for the `number` field. This is an advanced property which should be used if you know your use case requires it.  Use cases: - `false`: To allow non-E164 numbers like `+001234567890`, `1234`, or `abc`. This is useful for dialing out to non-E164 numbers on your SIP trunks. - `true` (default): To allow only E164 numbers like `+14155551234`. This is standard for PSTN calls.  If `false`, the `number` is still required to only contain alphanumeric characters (regex: `/^\+?[a-zA-Z0-9]+$/`).  @default true (E164 check is enabled) |
| `extension` | query | `string` | no | This is the extension that will be dialed after the call is answered. |
| `assistantOverrides` | query | `string` | no | These are the overrides for the assistant's settings and template variables specific to this customer. This allows customization of the assistant's behavior for individual customers in batch calls. |
| `number` | query | `string` | no | This is the number of the customer. |
| `sipUri` | query | `string` | no | This is the SIP URI of the customer. |
| `email` | query | `string` | no | This is the email of the customer. |
| `externalId` | query | `string` | no | This is the external ID of the customer. |
| `customerNumberAny` | query | `string` | no | Filter by any of the specified customer phone numbers (comma-separated). |
| `phoneNumberId` | query | `string` | no | This will return sessions with the specified phoneNumberId. |
| `phoneNumberIdAny[]` | query | `array<string>` | no | This will return sessions with any of the specified phoneNumberIds. |
| `page` | query | `number` | no | This is the page number to return. Defaults to 1. |
| `sortOrder` | query | `string` | no | This is the sort order for pagination. Defaults to 'DESC'. |
| `limit` | query | `number` | no | This is the maximum number of items to return. Defaults to 100. |
| `createdAtGt` | query | `string` | no | This will return items where the createdAt is greater than the specified value. |
| `createdAtLt` | query | `string` | no | This will return items where the createdAt is less than the specified value. |
| `createdAtGe` | query | `string` | no | This will return items where the createdAt is greater than or equal to the specified value. |
| `createdAtLe` | query | `string` | no | This will return items where the createdAt is less than or equal to the specified value. |
| `updatedAtGt` | query | `string` | no | This will return items where the updatedAt is greater than the specified value. |
| `updatedAtLt` | query | `string` | no | This will return items where the updatedAt is less than the specified value. |
| `updatedAtGe` | query | `string` | no | This will return items where the updatedAt is greater than or equal to the specified value. |
| `updatedAtLe` | query | `string` | no | This will return items where the updatedAt is less than or equal to the specified value. |
