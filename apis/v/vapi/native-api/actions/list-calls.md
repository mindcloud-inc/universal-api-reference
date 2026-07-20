# List Calls with Vapi

Retrieves a list of calls from Vapi.

## Endpoint

- **Method:** `GET`
- **Path:** `/call`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [List Calls](https://docs.vapi.ai/api-reference/calls/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | This is the unique identifier for the call. |
| `assistantId` | query | `string` | no | This will return calls with the specified assistantId. |
| `phoneNumberId` | query | `string` | no | This is the phone number that will be used for the call. To use a transient number, use `phoneNumber` instead.  Only relevant for `outboundPhoneCall` and `inboundPhoneCall` type. |
| `limit` | query | `number` | no | This is the maximum number of items to return. Defaults to 100. |
| `createdAtGt` | query | `string` | no | This will return items where the createdAt is greater than the specified value. |
| `createdAtLt` | query | `string` | no | This will return items where the createdAt is less than the specified value. |
| `createdAtGe` | query | `string` | no | This will return items where the createdAt is greater than or equal to the specified value. |
| `createdAtLe` | query | `string` | no | This will return items where the createdAt is less than or equal to the specified value. |
| `updatedAtGt` | query | `string` | no | This will return items where the updatedAt is greater than the specified value. |
| `updatedAtLt` | query | `string` | no | This will return items where the updatedAt is less than the specified value. |
| `updatedAtGe` | query | `string` | no | This will return items where the updatedAt is greater than or equal to the specified value. |
| `updatedAtLe` | query | `string` | no | This will return items where the updatedAt is less than or equal to the specified value. |
