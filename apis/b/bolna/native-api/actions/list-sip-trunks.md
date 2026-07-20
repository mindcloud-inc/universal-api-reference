# List SIP Trunks with Bolna

Retrieves SIP trunks configured in your Bolna account.

## Endpoint

- **Method:** `GET`
- **Path:** `/sip-trunks/trunks`
- **Base URL:** `https://api.bolna.ai`
- **Official documentation:** [List SIP Trunks](https://www.bolna.ai/docs/api-reference/sip-trunks/get_all)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_active` | query | `boolean` | no | Optional filter for active SIP trunks. |
