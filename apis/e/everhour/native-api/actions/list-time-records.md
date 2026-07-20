# List Time Records with Everhour

Retrieves time records from Everhour.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/time`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [List Time Records](https://everhour.docs.apiary.io/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Start date for the time range. |
| `to` | query | `string` | no | End date for the time range. |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `page` | query | `number` | no | Page number to return. |
