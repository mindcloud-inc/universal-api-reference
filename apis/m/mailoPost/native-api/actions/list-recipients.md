# List Recipients with MailoPost

Retrieves recipients from a MailoPost list.

## Endpoint

- **Method:** `GET`
- **Path:** `/email/lists/:id/recipients`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [List Recipients](https://mailopost.ru/api.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MailoPost recipient list identifier. |
