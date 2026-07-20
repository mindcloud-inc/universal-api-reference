# Upsert Group with Candu

Updates a group in Candu, or creates it if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/eventWebhook`
- **Base URL:** `https://api.candu.ai/api`
- **Official documentation:** [Upsert Group](https://developers.candu.ai/docs/get-data-into-candu-via-the-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | body | `string` | yes | The group ID to create or update. |
| `userId` | body | `string` | no | Optional user ID to associate with the group. |
| `traits` | body | `object` | no | Group traits to store in Candu. |
| `timestamp` | body | `date` | no | Optional event timestamp. |
