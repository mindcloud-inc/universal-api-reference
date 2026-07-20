# Get ACH Wallet Funding with OnlineCheckWriter

Retrieves the status and details of a specific ACH wallet funding request.

## Endpoint

- **Method:** `GET`
- **Path:** `/wallet/fund-wallet/:walletFundingId`
- **Base URL:** `https://test.onlinecheckwriter.com/api/v3`
- **Official documentation:** [Get ACH Wallet Funding](https://apiv3.onlinecheckwriter.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `walletFundingId` | path | `string` | yes | The wallet funding identifier. |
