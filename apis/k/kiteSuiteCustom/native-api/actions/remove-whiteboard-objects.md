# remove Whiteboard Objects with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/white-board/object/remove`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [remove Whiteboard Objects](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | body | `string` | yes | ID of the whiteboard containing the objects. |
| `body` | body | `object` | yes | Request body |
| `objects[]` | body | `array` | yes | Array of object IDs to delete. |
