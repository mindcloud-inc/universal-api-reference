# List Subaccount Orders with DigiCert

Retrieves orders from a DigiCert subaccount and its children.

## Endpoint

- **Method:** `GET`
- **Path:** `/account/subaccount/:subaccount_id/order`
- **Base URL:** `https://www.digicert.com/services/v2`
- **Official documentation:** [List Subaccount Orders](https://dev.digicert.com/certcentral-apis/services-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subaccount_id` | path | `string` | yes | The DigiCert subaccount identifier. |
