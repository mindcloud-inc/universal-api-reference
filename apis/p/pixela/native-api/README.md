# Pixela: Native API Reference

A consolidated summary of Pixela's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.pixe.la/
- **API base URL:** `https://pixe.la`

## Authentication

### Pixela User Token

Authenticate Pixela API requests with the user token provided at Pixela user registration.

### Credentials

- **Pixela user token:** `apiKey` · required

Send these headers with each API request:

```http
X-USER-TOKEN: <apiKey>
```

[Official authentication documentation](https://docs.pixe.la/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `500,503`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add To Pixel](actions/add-to-pixel.md) | `PUT /v1/users/:username/graphs/:graphID/add` | [docs](https://docs.pixe.la/entry/add-pixel) |
| [Add To Specific Pixel](actions/add-to-specific-pixel.md) | `PUT /v1/users/:username/graphs/:graphID/:yyyyMMdd/add` | [docs](https://docs.pixe.la/entry/add-specific-pixel) |
| [Create Graph](actions/create-graph.md) | `POST /v1/users/:username/graphs` | [docs](https://docs.pixe.la/entry/post-graph) |
| [Create Multiple Pixels](actions/create-multiple-pixels.md) | `POST /v1/users/:username/graphs/:graphID/pixels` | [docs](https://docs.pixe.la/entry/batch-post-pixels) |
| [Create Pixel](actions/create-pixel.md) | `POST /v1/users/:username/graphs/:graphID` | [docs](https://docs.pixe.la/entry/post-pixel) |
| [Create Webhook](actions/create-webhook.md) | `POST /v1/users/:username/webhooks` | [docs](https://docs.pixe.la/entry/post-webhook) |
| [Decrement Pixel](actions/decrement-pixel.md) | `PUT /v1/users/:username/graphs/:graphID/decrement` | [docs](https://docs.pixe.la/entry/decrement-pixel) |
| [Delete Graph](actions/delete-graph.md) | `DELETE /v1/users/:username/graphs/:graphID` | [docs](https://docs.pixe.la/entry/delete-graph) |
| [Delete Pixel](actions/delete-pixel.md) | `DELETE /v1/users/:username/graphs/:graphID/:yyyyMMdd` | [docs](https://docs.pixe.la/entry/delete-pixel) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v1/users/:username/webhooks/:webhookHash` | [docs](https://docs.pixe.la/entry/delete-webhook) |
| [Get Graph Definition](actions/get-graph-definition.md) | `GET /v1/users/:username/graphs/:graphID/graph-def` | [docs](https://docs.pixe.la/entry/get-graph-def) |
| [Get Graph Stats](actions/get-graph-stats.md) | `GET /v1/users/:username/graphs/:graphID/stats` | [docs](https://docs.pixe.la/entry/get-graph-stats) |
| [Get Graph SVG](actions/get-graph-svg.md) | `GET /v1/users/:username/graphs/:graphID` | [docs](https://docs.pixe.la/entry/get-svg) |
| [Get Latest Pixel](actions/get-latest-pixel.md) | `GET /v1/users/:username/graphs/:graphID/latest` | [docs](https://docs.pixe.la/entry/get-latest-pixel) |
| [Get Pixel](actions/get-pixel.md) | `GET /v1/users/:username/graphs/:graphID/:yyyyMMdd` | [docs](https://docs.pixe.la/entry/get-pixel) |
| [Get Today's Pixel](actions/get-todays-pixel.md) | `GET /v1/users/:username/graphs/:graphID/today` | [docs](https://docs.pixe.la/entry/get-today-pixel) |
| [Increment Pixel](actions/increment-pixel.md) | `PUT /v1/users/:username/graphs/:graphID/increment` | [docs](https://docs.pixe.la/entry/increment-pixel) |
| [List Graph Pixels](actions/list-graph-pixels.md) | `GET /v1/users/:username/graphs/:graphID/pixels` | [docs](https://docs.pixe.la/entry/get-graph-pixels) |
| [List Graphs](actions/list-graphs.md) | `GET /v1/users/:username/graphs` | [docs](https://docs.pixe.la/entry/get-graph) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v1/users/:username/webhooks` | [docs](https://docs.pixe.la/entry/get-webhook) |
| [Subtract From Pixel](actions/subtract-from-pixel.md) | `PUT /v1/users/:username/graphs/:graphID/subtract` | [docs](https://docs.pixe.la/entry/subtract-pixel) |
| [Subtract From Specific Pixel](actions/subtract-from-specific-pixel.md) | `PUT /v1/users/:username/graphs/:graphID/:yyyyMMdd/subtract` | [docs](https://docs.pixe.la/entry/subtract-specific-pixel) |
| [Update Graph](actions/update-graph.md) | `PUT /v1/users/:username/graphs/:graphID` | [docs](https://docs.pixe.la/entry/put-graph) |
| [Update Pixel](actions/update-pixel.md) | `PUT /v1/users/:username/graphs/:graphID/:yyyyMMdd` | [docs](https://docs.pixe.la/entry/put-pixel) |
