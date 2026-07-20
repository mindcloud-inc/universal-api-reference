# List senders with Webex Interact

Retrieves senders from Webex Interact.

## Endpoint

- **Method:** `GET`
- **Path:** `/assets/v1/senders`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [List senders](https://docs.webexinteract.com/reference/senders-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_number` | query | `string` | no | Page number to return. Defaults to 1. |
| `page_size` | query | `string` | no | Number of senders per page. Defaults to 25. Maximum 100. |
