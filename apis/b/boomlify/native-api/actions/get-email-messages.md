# Get Email Messages with Boomlify

Retrieves messages for a temporary email in Boomlify.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/emails/{id}/messages`
- **Base URL:** `https://v1.boomlify.com`
- **Official documentation:** [Get Email Messages](https://boomlify.com/en/temp-mail-api-docs?endpoint=get-messages&tab=docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Boomlify email UUID. |
