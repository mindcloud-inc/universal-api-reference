# Delete Source Key with Localazy

Deletes an existing source key from Localazy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:projectId/keys/:keyId`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Delete Source Key](https://localazy.com/docs/api/source-keys)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project id or slug. |
| `keyId` | path | `string` | yes | Source key identifier. |
