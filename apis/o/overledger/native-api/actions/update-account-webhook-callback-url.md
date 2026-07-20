# Update Account Webhook Callback URL with Overledger

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/webhooks/accounts/:webhookId`
- **Base URL:** `https://api.overledger.dev`
- **Official documentation:** [Update Account Webhook Callback URL](https://docs.overledger.dev/docs/update-the-callback-url-for-an-account-webhook)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `API-Version` | `3.0.0` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | path | `string` | yes | Account webhook identifier to update. |
| `callbackUrl` | body | `string` | yes | New public callback URL for the account webhook. |
