# Update Source Key with Localazy

Updates an existing source key in Localazy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId/keys/:keyId`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Update Source Key](https://localazy.com/docs/api/source-keys)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project id or slug. |
| `keyId` | path | `string` | yes | Source key identifier. |
| `deprecated` | body | `number` | no | Set to -1 to remove deprecation or to 0+ to mark the key deprecated. |
| `hidden` | body | `boolean` | no | Hide the key from translation in Localazy. |
| `comment` | body | `string` | no | Comment for translators. |
| `limit` | body | `number` | no | Translation character limit or -1 to disable. |
