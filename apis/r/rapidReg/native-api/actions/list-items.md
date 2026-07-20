# List Items with RapidReg

Retrieves items from RapidReg.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/get/items`
- **Base URL:** `https://rapidreg.com`
- **Official documentation:** [List Items](https://rapidreg.com/developers#dev-items)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | body | `string` | no | Optional brand UUID to filter items. |
