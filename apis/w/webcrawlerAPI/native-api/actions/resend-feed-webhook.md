# Resend Feed Webhook with Webcrawler API

Resends a feed webhook from Webcrawler API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/feed/:id/webhook/resend`
- **Base URL:** `https://api.webcrawlerapi.com`
- **Official documentation:** [Resend Feed Webhook](https://webcrawlerapi.com/docs/api/feed/feed-manage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Feed identifier returned by List Feeds or Create Feed. |
