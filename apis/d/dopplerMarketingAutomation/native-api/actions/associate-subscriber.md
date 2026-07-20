# Associate Subscriber with Doppler Marketing Automation

Creates a subscriber association in Doppler Marketing Automation.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountName/lists/:listId/subscribers`
- **Base URL:** `https://restapi.fromdoppler.com`
- **Official documentation:** [Associate Subscriber](https://restapi.fromdoppler.com/docs/rels/associate-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | Doppler list identifier. |
| `email` | body | `string` | yes | Subscriber email address. |
| `fields[]` | body | `array<object>` | no | Subscriber field values. |
