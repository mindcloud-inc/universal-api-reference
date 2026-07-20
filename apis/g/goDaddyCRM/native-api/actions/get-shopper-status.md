# Get Shopper Status with GoDaddy CRM

Retrieves shopper status from your GoDaddy account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/shoppers/:shopperId/status`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Get Shopper Status](https://developer.godaddy.com/doc/endpoint/shoppers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shopperId` | path | `string` | yes | Required shopper identifier to retrieve status for |
| `auditClientIp` | query | `string` | yes | Required originating client IP address |
