# List Hooks with Make

Lists hooks for the specified team.

## Endpoint

- **Method:** `GET`
- **Path:** `/hooks`
- **Base URL:** `https://us2.make.com/api/v2`
- **Official documentation:** [List Hooks](https://developers.make.com/api-documentation/api-reference/hooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | query | `number` | yes | The ID of the Make team whose hooks should be listed. |
