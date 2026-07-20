# Remove Contact From Power Dialer Lists with Aloware

Removes a contact from Aloware power dialer lists.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhook/powerdialer-remove-contact-from-lists`
- **Base URL:** `https://app.aloware.com`
- **Official documentation:** [Remove Contact From Power Dialer Lists](https://support.aloware.com/en/articles/9167815-aloware-power-dialer-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `string` | yes | Aloware contact ID to remove from every power dialer list. |
