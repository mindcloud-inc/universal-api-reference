# Update Webhook with SMSGatewayCenter SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/SMSApi/webhook/update`
- **Base URL:** `https://unify.smsgateway.center`
- **Official documentation:** [Update Webhook](https://www.smsgatewaycenter.com/developer-api/update-webhook/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `smswebhook` | body | `string` | yes | URL that will receive SMS delivery reports. |
| `smswebhookrate` | body | `number` | yes | DLR TPS rate for forwarding webhook events. |
