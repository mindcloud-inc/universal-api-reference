# Retrieve Domain Purchase Agreements with GoDaddy CRM

Retrieves domain purchase agreements from GoDaddy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/domains/agreements`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Retrieve Domain Purchase Agreements](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tlds[]` | query | `array<string>` | yes | List of TLDs whose legal agreements should be retrieved. |
| `privacy` | query | `boolean` | yes | Whether privacy has been requested. |
| `forTransfer` | query | `boolean` | no | Whether a domain transfer has been requested. |
