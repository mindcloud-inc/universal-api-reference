# Matterport: Native API Reference

A consolidated summary of Matterport's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://matterport.github.io/showcase-sdk/api_home.html
- **API base URL:** `https://api.matterport.com/`

## Authentication

### API Token

Use your Matterport API Token ID as the username and Token Secret as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://matterport.github.io/showcase-sdk/api_home.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Model Access](actions/get-model-access.md) | `POST api/models/graph` | [docs](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/accessinfo.doc.html) |
| [Get Model Bundles](actions/get-model-bundles.md) | `POST api/models/graph` | [docs](https://matterport.github.io/showcase-sdk/modelapi_ordering_addons.html) |
| [Get Model Details](actions/get-model-details.md) | `POST api/models/graph` | [docs](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/model.doc.html) |
| [Get Model Floors](actions/get-model-floors.md) | `POST api/models/graph` | [docs](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/modelfloor.doc.html) |
| [Get Model Geo Coordinates](actions/get-model-geo-coordinates.md) | `POST api/models/graph` | [docs](https://matterport.github.io/showcase-sdk/modelapi_geocoordinates.html) |
| [Get Model Image](actions/get-model-image.md) | `POST api/models/graph` | [docs](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/photo.doc.html) |
| [Get Model Labels](actions/get-model-labels.md) | `POST api/models/graph` | [docs](https://static.matterport.com/api-doc/2024.07.44-main-g63d157b/reference/graphdoc/model/label.doc.html) |
| [Get Model Locations](actions/get-model-locations.md) | `POST api/models/graph` | [docs](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/anchorlocation.doc.html) |
| [Get Model Mattertags](actions/get-model-mattertags.md) | `POST api/models/graph` | [docs](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/mattertag.doc.html) |
| [Get Model Measurement Paths](actions/get-model-measurement-paths.md) | `POST api/models/graph` | [docs](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/measurementpath.doc.html) |
| [Get Model Notes](actions/get-model-notes.md) | `POST api/models/graph` | [docs](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/note.doc.html) |
| [Get Model Pano Locations](actions/get-model-pano-locations.md) | `POST api/models/graph` | [docs](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/panoramicimagelocation.doc.html) |
| [Get Model Rooms](actions/get-model-rooms.md) | `POST api/models/graph` | [docs](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/modelroom.doc.html) |
| [Get Model Uploaders](actions/get-model-uploaders.md) | `POST api/models/graph` | [docs](https://static.matterport.com/api-doc/2025.10.58-main-gf3922d9/reference/graphdoc/model/usermetadata.doc.html) |
| [Get Model Views](actions/get-model-views.md) | `POST api/models/graph` | [docs](https://matterport.github.io/showcase-sdk/modelapi_views_and_layers.html) |
| [GraphQL Query](actions/graph-ql-query.md) | `POST api/models/graph` | [docs](https://api.matterport.com/docs/reference) |
| [List Models](actions/list-models.md) | `POST api/models/graph` | [docs](https://matterport.github.io/showcase-sdk/modelapi_models_ref.html) |
