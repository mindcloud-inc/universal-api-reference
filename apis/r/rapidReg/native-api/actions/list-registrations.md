# List Registrations with RapidReg

Retrieves registrations from RapidReg.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/get/registrations`
- **Base URL:** `https://rapidreg.com`
- **Official documentation:** [List Registrations](https://rapidreg.com/developers#dev-reg)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | body | `string` | no | Optional brand UUID to filter registrations. |
| `item_id` | body | `string` | no | Optional item UUID to filter registrations. |
| `start` | body | `number` | no | Optional UTC timestamp lower bound. |
| `end` | body | `number` | no | Optional UTC timestamp upper bound. |
| `limit` | body | `number` | no | Optional maximum number of registrations to return. |
