# Get Screenshot with PeekShot

Retrieves a screenshot by request ID from PeekShot.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshots/:requestId`
- **Base URL:** `https://api.peekshot.com/api/v1`
- **Official documentation:** [Get Screenshot](https://docs.peekshot.com/api-reference/get-screenshot-7azv)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `number` | yes | Unique ID of the screenshot request. |
