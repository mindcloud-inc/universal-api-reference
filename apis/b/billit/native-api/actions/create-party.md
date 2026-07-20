# Create Party with Billit

Creates a new party in Billit.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/parties`
- **Base URL:** `https://api.sandbox.billit.be`
- **Official documentation:** [Create Party](https://docs.billit.be/reference/party_postparty-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Company or contact display name. |
| `PartyType` | body | `string` | yes | Billit party type such as Customer or Supplier. |
| `VATNumber` | body | `string` | no | VAT number when available. |
| `Addresses[]` | body | `array<object>` | no | Billit address array. |
| `Identifiers[]` | body | `array<object>` | no | Optional alternate identifier array. |
