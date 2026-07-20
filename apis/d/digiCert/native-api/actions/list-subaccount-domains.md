# List Subaccount Domains with DigiCert

Retrieves domain details from a DigiCert subaccount.

## Endpoint

- **Method:** `GET`
- **Path:** `/account/subaccount/:subaccount_id/domain`
- **Base URL:** `https://www.digicert.com/services/v2`
- **Official documentation:** [List Subaccount Domains](https://dev.digicert.com/certcentral-apis/services-api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subaccount_id` | path | `string` | yes | The DigiCert subaccount identifier. |
