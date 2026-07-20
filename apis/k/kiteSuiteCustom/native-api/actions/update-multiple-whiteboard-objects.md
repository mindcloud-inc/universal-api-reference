# Update Multiple Whiteboard Objects with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/white-board/object/multiple`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Multiple Whiteboard Objects](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `objects[]` | body | `array` | yes | Array of objects to update. |
| `isGroup` | body | `boolean` | yes | Group status of the objects. |
