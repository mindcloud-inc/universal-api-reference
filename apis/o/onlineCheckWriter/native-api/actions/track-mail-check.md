# Track Mail Check with OnlineCheckWriter

Retrieves tracking details for a mailed check.

## Endpoint

- **Method:** `GET`
- **Path:** `/mailchecks/:checkId/tracking`
- **Base URL:** `https://test.onlinecheckwriter.com/api/v3`
- **Official documentation:** [Track Mail Check](https://apiv3.onlinecheckwriter.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkId` | path | `string` | yes | The check identifier. |
