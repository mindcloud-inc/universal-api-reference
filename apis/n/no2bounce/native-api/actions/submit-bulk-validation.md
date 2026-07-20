# Submit Bulk Validation with no2bounce

Creates a bulk validation job in no2bounce.

## Endpoint

- **Method:** `POST`
- **Path:** `/n2b_validate_bulk`
- **Base URL:** `https://connect.no2bounce.com/v2`
- **Official documentation:** [Submit Bulk Validation](https://www.no2bounce.com/api-documentation#making-api-request)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailList[]` | body | `array<string>` | yes | Provide one or more email addresses to validate. |
