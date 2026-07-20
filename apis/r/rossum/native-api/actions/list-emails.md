# List Emails with Rossum

Retrieves emails from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/emails`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [List Emails](https://rossum.app/api/docs/openapi/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queue` | query | `number` | no | Filter emails by Rossum queue ID. |
| `page_size` | query | `number` | no | Number of emails to return. |
