# List Actors with Apify

Retrieves actors from Apify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/acts`
- **Base URL:** `https://api.apify.com`
- **Official documentation:** [List Actors](https://docs.apify.com/api/v2/acts-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `my` | query | `boolean` | no | If true, return only actors owned by the authenticated user. |
