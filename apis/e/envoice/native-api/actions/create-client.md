# Create Client with Envoice

Creates a new client in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `client/new`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Create Client](https://github.com/EmitKnowledge/Envoice/blob/master/client.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientCurrencyId` | body | `number` | yes | Currency ID for the client. |
| `ClientCountryId` | body | `number` | yes | Country ID for the client. |
| `UiLanguageId` | body | `number` | yes | UI language ID for the client. |
| `Name` | body | `string` | yes | Client display name. |
| `Email` | body | `string` | yes | Primary client email address. |
