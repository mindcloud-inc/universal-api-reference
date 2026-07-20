# List Notes with Zoho Recruit

Retrieves all notes from Zoho Recruit.

## Endpoint

- **Method:** `GET`
- **Path:** `/Notes`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [List Notes](https://www.zoho.com/recruit/developer-guide/apiv2/get-notes.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number of notes to fetch. |
| `per_page` | query | `number` | no | Maximum number of notes to fetch per page. |
