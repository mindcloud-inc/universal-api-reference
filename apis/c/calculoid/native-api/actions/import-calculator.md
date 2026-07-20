# Import Calculator with Calculoid

## Endpoint

- **Method:** `POST`
- **Path:** `/calculators/import`
- **Base URL:** `https://api.calculoid.com`
- **Official documentation:** [Import Calculator](https://www.calculoid.com/documentation-new)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `calculator` | body | `object` | yes | Calculator import payload exported from Calculoid. |
