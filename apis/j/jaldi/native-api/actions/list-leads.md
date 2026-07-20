# List Leads with Jaldi

Retrieves leads from Jaldi.

## Endpoint

- **Method:** `POST`
- **Path:** `/add_on/webhook/fetch_crm_data`
- **Base URL:** `https://api.jalditech.com`
- **Official documentation:** [List Leads](https://jalditech.com/support/sending-leads-to-jaldi-via-webhooks-connect-to-website-lead-forms/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `last_update_from` | query | `string` | no | Return leads updated on or after this Jaldi datetime in YYYY-MM-DD hh:mm format. |
| `last_update_to` | query | `string` | no | Return leads updated on or before this Jaldi datetime in YYYY-MM-DD hh:mm format. |
