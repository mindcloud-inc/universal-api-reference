# List Parties with Billit

Retrieves Billit parties for the authenticated company.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/parties`
- **Base URL:** `https://api.sandbox.billit.be`
- **Official documentation:** [List Parties](https://docs.billit.be/reference/party_getparties-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData filter for Billit parties. |
