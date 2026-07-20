# List Collections with Snappy

Retrieves collections from Snappy.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [List Collections](https://docs.snappy.com/reference/getcollections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `budget` | query | `number` | yes | Budget value. |
| `companyId` | query | `string` | no | Company ID. |
| `accountId` | query | `string` | no | Account ID. |
| `countries[]` | query | `array<string>` | no | List of supported countries. |
| `types[]` | query | `array<string>` | no | List of collection types. |
| `fields[]` | query | `array<string>` | no | Additional collection fields to include. |
| `skip` | query | `number` | no | Number of records to skip for pagination. |
| `limit` | query | `number` | no | Maximum number of records to return per page. |
