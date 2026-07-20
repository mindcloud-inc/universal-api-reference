# <img src="https://images.mindcloud.co/apps/icons/matterport_1776278486795.png" alt="Matterport logo" width="28" height="28"> Matterport: Universal API

Access Matterport's GraphQL APIs for searching spaces, reading model details, managing model metadata, and working with model assets.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/matterport/latest
- **Category:** Support / Field Service
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://matterport.com
- **Vendor API docs:** https://matterport.github.io/showcase-sdk/api_home.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matterport/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Bundles](actions/get-model-bundles.md) | GET | Retrieves add-on bundles from a Matterport model. |
| [Get Model Details](actions/get-model-details.md) | GET | Retrieves details for a Matterport model. |
| [List Models](actions/list-models.md) | GET | Retrieves models from your Matterport account. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Image](actions/get-model-image.md) | GET | Retrieves image details for a Matterport model. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Labels](actions/get-model-labels.md) | GET | Retrieves labels from a Matterport model. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Floors](actions/get-model-floors.md) | GET | Retrieves floors from a Matterport model. |
| [Get Model Geo Coordinates](actions/get-model-geo-coordinates.md) | GET | Retrieves geo coordinates for a Matterport model. |
| [Get Model Locations](actions/get-model-locations.md) | GET | Retrieves anchor locations from a Matterport model. |
| [Get Model Pano Locations](actions/get-model-pano-locations.md) | GET | Retrieves panoramic image locations from a Matterport model. |
| [Get Model Rooms](actions/get-model-rooms.md) | GET | Retrieves rooms from a Matterport model. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Notes](actions/get-model-notes.md) | GET | Retrieves notes from a Matterport model. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Access](actions/get-model-access.md) | GET | Retrieves access details for a Matterport model. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [GraphQL Query](actions/graph-ql-query.md) | GET | Makes an authenticated GraphQL request to Matterport. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Mattertags](actions/get-model-mattertags.md) | GET | Retrieves Mattertags from a Matterport model. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Measurement Paths](actions/get-model-measurement-paths.md) | GET | Retrieves measurement paths from a Matterport model. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Uploaders](actions/get-model-uploaders.md) | GET | Retrieves uploader details for a Matterport model. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [Get Model Views](actions/get-model-views.md) | GET | Retrieves saved views from a Matterport model. |

