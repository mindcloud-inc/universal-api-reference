# Enrich Contacts with Dropcontact

Creates a contact enrichment request in Dropcontact.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/enrich/all`
- **Base URL:** `https://api.dropcontact.com`
- **Official documentation:** [Enrich Contacts](https://developer.dropcontact.com/#post-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_callback_url` | body | `string` | no | Optional per-request webhook callback URL. |
| `data` | body | `list<object>` | yes | Contact records to enrich. Dropcontact accepts up to 250 contacts per request. |
| `language` | body | `string` | no | Language used by Dropcontact for enrichment heuristics, for example en or fr. |
| `siren` | body | `boolean` | no | Whether to return SIREN data when available. |
