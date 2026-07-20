# Import Subscribers To List with Doppler Marketing Automation

Creates a subscriber import job in Doppler Marketing Automation.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountName/lists/:listId/subscribers/import`
- **Base URL:** `https://restapi.fromdoppler.com`
- **Official documentation:** [Import Subscribers To List](https://restapi.fromdoppler.com/docs/rels/import-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Doppler list identifier. |
| `fields[]` | body | `array<string>` | yes | Required field-name list for import. Use an empty array when importing email-only subscribers. |
| `items[]` | body | `array<object>` | yes | Subscribers to import. |
| `callback` | body | `string` | no | Optional callback URL invoked when the import task completes. |
