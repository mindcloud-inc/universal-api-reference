# Get Client with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/client/get`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Get Client](https://api.quickfile.co.uk/d/v1_2/Client_Get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | The QuickFile ClientID to retrieve. |
| `Address` | body | `boolean` | no | When true, includes the client postal address. |
| `VATDetails` | body | `boolean` | no | When true, includes VAT number and EC status. |
| `Preferences` | body | `boolean` | no | When true, includes QuickFile client preferences. |
| `ClientContacts` | body | `boolean` | no | When true, includes associated client contacts. |
| `Financials` | body | `boolean` | no | When true, includes balances and credits on account. |
| `GoCardlessDetails` | body | `boolean` | no | When true, includes GoCardless pre-auth details when available. |
