# Search By Email (outside EU) with Datagma

Finds contacts in Datagma by email outside the EU.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/reverse_email`
- **Base URL:** `https://gateway.datagma.net/api/ingress`
- **Official documentation:** [Search By Email (outside EU)](https://datagmaapi.readme.io/reference/ingressservice_searchbyemail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Target email address to search by. |
