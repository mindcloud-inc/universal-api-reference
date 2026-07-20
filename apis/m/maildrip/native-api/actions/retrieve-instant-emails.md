# Retrieve instant emails with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/instant-emails`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Retrieve instant emails](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter by status (draft, scheduled, queued, processing, completed, processed) |
| `search` | query | `string` | no | Search term to filter by email title |
| `page` | query | `number` | no | Page number for pagination |
| `limit` | query | `string` | no | Number of items per page, use "all" for all items |
