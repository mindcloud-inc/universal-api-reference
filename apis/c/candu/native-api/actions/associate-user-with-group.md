# Associate User With Group with Candu

Associates a user with a group in Candu.

## Endpoint

- **Method:** `POST`
- **Path:** `/eventWebhook`
- **Base URL:** `https://api.candu.ai/api`
- **Official documentation:** [Associate User With Group](https://developers.candu.ai/docs/get-data-into-candu-via-the-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | The target group ID. |
| `userId` | body | `string` | yes | The user ID to associate to the group. |
| `traits` | body | `object` | no | Optional group traits to update at the same time. |
| `timestamp` | body | `date` | no | Optional event timestamp. |
