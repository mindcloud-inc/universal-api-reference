# Create Access Link with Oneflow

Creates an access link in Oneflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/contracts/:contractId/participants/:participantId/access_link`
- **Base URL:** `https://api.oneflow.com/v1`
- **Official documentation:** [Create Access Link](https://developer.oneflow.com/reference/create-an-access-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contractId` | path | `string` | yes | The Oneflow contract ID. |
| `participantId` | path | `string` | yes | The Oneflow contract participant ID. |
