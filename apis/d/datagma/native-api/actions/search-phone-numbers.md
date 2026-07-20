# Search Phone Numbers with Datagma

Finds phone numbers in Datagma by email or profile.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/search`
- **Base URL:** `https://gateway.datagma.net/api/ingress`
- **Official documentation:** [Search Phone Numbers](https://datagmaapi.readme.io/reference/ingressservice_search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | query | `string` | no | Social profile URL or username used as the starting point for phone lookup. |
| `email` | query | `string` | no | Email address used as the starting point for phone lookup. |
| `minimumMatch` | query | `string` | no | Minimum match threshold for the phone search. |
| `whatsappCheck` | query | `string` | no | Set true to verify whether a matched number is linked to WhatsApp. |
