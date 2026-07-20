# Update Client with Envoice

Updates an existing client in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `client/update`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Update Client](https://github.com/EmitKnowledge/Envoice/blob/master/client.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `number` | yes | Client ID. |
| `ClientCurrencyId` | body | `number` | yes | Currency ID for the client. |
| `ClientCountryId` | body | `number` | yes | Country ID for the client. |
| `UiLanguageId` | body | `number` | yes | UI language ID for the client. |
| `Name` | body | `string` | yes | Client display name. |
| `Email` | body | `string` | yes | Primary client email address. |
