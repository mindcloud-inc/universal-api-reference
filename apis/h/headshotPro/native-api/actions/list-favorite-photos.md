# List Favorite Photos with HeadshotPro

Retrieves favorite photos from HeadshotPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/organization/photos/favorites`
- **Base URL:** `https://server.headshotpro.com/api/v2`
- **Official documentation:** [List Favorite Photos](https://www.headshotpro.com/api/photos)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | query | `string` | no | Optional team filter for organization favorite photos. |
| `include` | query | `string` | no | URL variants to include: main or all. |
