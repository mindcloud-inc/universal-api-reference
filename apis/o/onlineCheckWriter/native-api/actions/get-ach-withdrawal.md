# Get ACH Withdrawal with OnlineCheckWriter

Retrieves the status and details of a specific ACH withdrawal.

## Endpoint

- **Method:** `GET`
- **Path:** `/wallet/withdraw/ach/:withdrawalId`
- **Base URL:** `https://test.onlinecheckwriter.com/api/v3`
- **Official documentation:** [Get ACH Withdrawal](https://apiv3.onlinecheckwriter.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `withdrawalId` | path | `string` | yes | The withdrawal identifier. |
