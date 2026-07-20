# Download Certificate with GoDaddy CRM

Downloads a customer certificate from GoDaddy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/certificates/download`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Download Certificate](https://developer.godaddy.com/doc/endpoint/certificates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entitlementId` | query | `string` | yes | Required entitlement identifier to download |
