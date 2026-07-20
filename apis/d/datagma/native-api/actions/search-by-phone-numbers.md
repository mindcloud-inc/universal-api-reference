# Search By Phone Numbers with Datagma

Finds contacts in Datagma by phone number.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/reverse_phone_lookup`
- **Base URL:** `https://gateway.datagma.net/api/ingress`
- **Official documentation:** [Search By Phone Numbers](https://datagmaapi.readme.io/reference/ingressservice_searchbyphone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | query | `string` | no | Phone number to look up. |
