# List Team Messages with Heymarket SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/all`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [List Team Messages](https://heymarket.docs.apiary.io/api-description-document)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_at` | body | `string` | no | Fetch messages created on and after this RFC 3339 timestamp. |
