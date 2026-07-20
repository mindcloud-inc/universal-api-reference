# Import Unsubscribed Subscribers with Doppler Marketing Automation

Creates an unsubscribed import job in Doppler Marketing Automation.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountName/unsubscribed/import`
- **Base URL:** `https://restapi.fromdoppler.com`
- **Official documentation:** [Import Unsubscribed Subscribers](https://restapi.fromdoppler.com/docs/rels/import-unsubscribed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[]` | body | `array<object>` | yes | Unsubscribed subscribers to import. |
| `callback` | body | `string` | no | Optional callback URL invoked when the import task completes. |
