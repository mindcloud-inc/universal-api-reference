# List Invoices with Harpoon

Retrieves invoices from Harpoon.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://app.harpoonapp.com/api`
- **Official documentation:** [List Invoices](https://app.harpoonapp.com/api)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `year` | query | `string` | no |
| `clients[]` | query | `array<number>` | no |
| `projects[]` | query | `array<number>` | no |
| `statuses[]` | query | `array<string>` | no |
| `search` | query | `string` | no |
