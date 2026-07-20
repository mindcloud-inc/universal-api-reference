# Update Whiteboard Object Position with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/white-board/object/position`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Whiteboard Object Position](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `object` | body | `string` | yes | ID of the object to reposition. |
| `position` | body | `number` | yes | New position of the object in the whiteboard's object list. |
