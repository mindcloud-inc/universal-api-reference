# Get Dashboard Email Messages with Boomlify

Retrieves received messages for a dashboard email in Boomlify.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/emails/{id}/messages`
- **Base URL:** `https://v1.boomlify.com`
- **Official documentation:** [Get Dashboard Email Messages](https://boomlify.com/en/temp-mail-api-docs?endpoint=get-dashboard-messages&tab=docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Boomlify dashboard email UUID. |
