# List Credentials with Sertifier

Finds credentials in Sertifier by search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/credential/search`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [List Credentials](https://sertifier.docs.apiary.io/reference/credential/search-credentials)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startIndex` | body | `number` | no | — |
| `length` | body | `number` | no | — |
| `status` | body | `number` | no | — |
| `searchTerm` | body | `string` | no | — |
| `campaignIds[]` | body | `array<string>` | no | Send multiple values as a array. |
| `recipientIds[]` | body | `array<string>` | no | Send multiple values as a array. |
