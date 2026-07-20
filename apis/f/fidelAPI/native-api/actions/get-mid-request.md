# Get MID Request with Fidel API

Retrieves a MID request from Fidel API.

## Endpoint

- **Method:** `GET`
- **Path:** `/programs/:programId/mid-requests/:midRequestId`
- **Base URL:** `https://api.fidel.uk/v1`
- **Official documentation:** [Get MID Request](https://reference.fidel.uk/reference/get-mid-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `programId` | path | `string` | yes | — |
| `midRequestId` | path | `string` | yes | The MID request ID. |
