# Create Client with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/client/create`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Create Client](https://api.quickfile.co.uk/d/v1_2/Client_Create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CompanyName` | body | `string` | yes | Client company or trading name to create. |
| `AccountReference` | body | `string` | no | Optional external reference or short account code for the client. |
| `Town` | body | `string` | no | Town or city for the postal address. |
| `AddressLine1` | body | `string` | no | First postal address line. |
| `Postcode` | body | `string` | no | Postal or ZIP code. |
| `CountryISO` | body | `string` | no | Two-letter ISO country code for the address when supported. |
| `AllowAttachPDF` | body | `boolean` | no | When true, enables emailing PDF invoices to this client. |
