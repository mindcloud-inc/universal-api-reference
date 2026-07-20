# Search Recipients with MailoPost

Finds recipients in MailoPost by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/email/recipients/search`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Search Recipients](https://mailopost.ru/api.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address to search for. |
