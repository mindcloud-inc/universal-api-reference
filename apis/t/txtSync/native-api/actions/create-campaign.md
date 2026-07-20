# Create Campaign with TxtSync

Creates a new campaign in TxtSync.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns`
- **Base URL:** `https://api.txtsync.com`
- **Official documentation:** [Create Campaign](https://docs.txtsync.com/#add-campaign)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Name` | body | `string` | yes |
| `NumberID` | body | `number` | no |
| `TextMessage` | body | `string` | no |
