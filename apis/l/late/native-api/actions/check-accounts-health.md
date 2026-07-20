# Check Accounts Health with Late

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/health`
- **Base URL:** `https://zernio.com/api/v1`
- **Official documentation:** [Check Accounts Health](https://docs.zernio.com/accounts/check-accounts-health)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profileId` | query | `string` | no | — |
| `platform` | query | `list` | no | Accepted values: `bluesky`, `facebook`, `googlebusiness`, `instagram`, `linkedin`, `pinterest`, `reddit`, `snapchat`, `telegram`, `threads`, `tiktok`, `twitter`, `youtube`. |
| `status` | query | `list` | no | Accepted values: `error`, `healthy`, `warning`. |
