# Clear Power Dialer List with Aloware

Clears all contacts from an Aloware power dialer list.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhook/powerdialer-clear-list`
- **Base URL:** `https://app.aloware.com`
- **Official documentation:** [Clear Power Dialer List](https://support.aloware.com/en/articles/9167815-aloware-power-dialer-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | Power dialer list ID to clear. |
