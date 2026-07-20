# Undo Whiteboard Object Deletion with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/white-board/object/undo-redo`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Undo Whiteboard Object Deletion](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | body | `string` | yes | ID of the object to restore. |
| `body` | body | `object` | yes | Request body |
| `nodes[]` | body | `array` | yes | Array of node objects to restore. |
| `index` | body | `number` | yes | Position of the restored object in the whiteboard's object list. |
| `type` | body | `string` | yes | Type of object being restored. |
