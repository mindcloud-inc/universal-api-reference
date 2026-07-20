# List Vacancies with Jaicob

## Endpoint

- **Method:** `GET`
- **Path:** `/vacancies/public`
- **Base URL:** `https://api.jaicob.ai`
- **Official documentation:** [List Vacancies](https://developers.jaicob.ai/reference/list_vacancies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `clientId` | query | `string` | no |
| `locationId` | query | `string` | no |
| `query` | query | `string` | no |
| `city` | query | `string` | no |
| `onlyRemote` | query | `boolean` | no |
| `jobCategoryIds[]` | query | `array<number>` | no |
| `industryIds[]` | query | `array<number>` | no |
| `seniorityIds[]` | query | `array<number>` | no |
| `educationLevelIds[]` | query | `array<number>` | no |
