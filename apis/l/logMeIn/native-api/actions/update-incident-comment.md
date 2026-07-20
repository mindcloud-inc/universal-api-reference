# Update Incident Comment with LogMeIn

Updates an existing incident comment in LogMeIn.

## Endpoint

- **Method:** `PUT`
- **Path:** `/goto-resolve-ticketing/v1/incidents/:referenceNum/comments/:commentId`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Update Incident Comment](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceNum` | path | `string` | yes | Required incident reference number. |
| `commentId` | path | `string` | yes | Required comment ID. |
| `comment` | body | `string` | yes | Updated comment text. |
| `hiddenFromCustomerAt` | body | `date` | no | Updated hidden-from-customer timestamp. |
