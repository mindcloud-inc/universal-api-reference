# Set WhatsApp Retrieval Status with Smsmobileapi

Updates WhatsApp retrieval status in Smsmobileapi.

## Endpoint

- **Method:** `GET`
- **Path:** `/getwa/active/`
- **Base URL:** `https://api.smsmobileapi.com`
- **Official documentation:** [Set WhatsApp Retrieval Status](https://smsmobileapi.com/doc-whatsapp/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `statut` | query | `list` | yes | Set WhatsApp retrieval to activated or deactivated explicitly. Accepted values: `0`, `1`. |
