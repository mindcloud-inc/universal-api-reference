# Update Client with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/client/update`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Update Client](https://api.quickfile.co.uk/d/v1_2/Client_Update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | QuickFile ClientID to update. |
| `CompanyName` | body | `string` | no | Updated client company or trading name. |
| `AccountReference` | body | `string` | no | Updated external reference or short account code. |
| `Town` | body | `string` | no | Updated town or city. |
| `AddressLine1` | body | `string` | no | Updated first postal address line. |
| `Postcode` | body | `string` | no | Updated postal or ZIP code. |
| `CountryISO` | body | `string` | no | Updated two-letter ISO country code when supported. |
| `AllowAttachPDF` | body | `boolean` | no | When true, keeps PDF email delivery enabled for this client. |
