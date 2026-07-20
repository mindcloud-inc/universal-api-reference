# Update Party with Billit

Updates an existing party in Billit.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/parties/:partyID`
- **Base URL:** `https://api.sandbox.billit.be`
- **Official documentation:** [Update Party](https://docs.billit.be/reference/party_patchparties-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `partyID` | path | `number` | yes | Billit PartyID. |
| `Name` | body | `string` | no | Updated display name. |
| `VATNumber` | body | `string` | no | Updated VAT number. |
| `Addresses[]` | body | `array<object>` | no | Updated addresses array. |
