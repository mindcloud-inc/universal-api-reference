# Get Resources by Phone Number with Sage Sales Management

Finds resources in Sage Sales Management by phone number.

## Endpoint

- **Method:** `GET`
- **Path:** `/calls/phone/{{phoneNumber}}`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Get Resources by Phone Number](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | path | `string` | yes | Phone number |
