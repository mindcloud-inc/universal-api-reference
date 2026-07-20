# Search Certificates with GoDaddy CRM

Retrieves certificates from your GoDaddy account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/certificates`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Search Certificates](https://developer.godaddy.com/doc/endpoint/certificates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entitlementId` | query | `string` | yes | Entitlement ID to look up. |
| `latest` | query | `boolean` | no | Fetch only the most recent certificate. |
