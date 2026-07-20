# List Layouts with Zoho Desk

Retrieve a list of all the layouts configured for a module.

## Endpoint

- **Method:** `GET`
- **Path:** `layouts`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [List Layouts](https://desk.zoho.com/DeskAPIDocument#Layouts#Layouts_ListLayouts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module` | query | `list<string>` | yes | Name of the module whose layouts must be fetched. Accepted values: `accounts`, `calls`, `contacts`, `contracts`, `events`, `products`, `tasks`, `tickets`, `timeEntry`. |
| `status` | query | `list<string>` | yes | Status of the layout. |
| `layoutName` | query | `string` | no | Name of the layout. Maximum length: 200. |
| `id` | query | `number` | no | — |
| `departmentId` | query | `number` | no | — |
