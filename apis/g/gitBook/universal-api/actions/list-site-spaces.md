# GitBook: List Site Spaces

Retrieves spaces attached to a GitBook site.

```
GET https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-site-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-site-spaces?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string",
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-site-spaces?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `default` | boolean | no |  |
| `organizationId` | string | yes |  |
| `shareKey` | string | no |  |
| `siteId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "default": true,
      "draft": true,
      "hasAdvancedCustomizationFeature": true,
      "hidden": true,
      "id": "string",
      "object": "string",
      "path": "string",
      "space": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "defaultLevel": "string",
        "editMode": "string",
        "emoji": "string",
        "id": "string",
        "organization": "string",
        "revision": "string",
        "title": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "urls": {
          "app": "https://example.com",
          "location": "https://example.com"
        },
        "visibility": "string"
      },
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default` | boolean |  |
| `draft` | boolean |  |
| `hasAdvancedCustomizationFeature` | boolean |  |
| `hidden` | boolean |  |
| `id` | string |  |
| `object` | string |  |
| `path` | string |  |
| `space.createdAt` | date |  |
| `space.defaultLevel` | string |  |
| `space.editMode` | string |  |
| `space.emoji` | string |  |
| `space.id` | string |  |
| `space.organization` | string |  |
| `space.revision` | string |  |
| `space.title` | string |  |
| `space.updatedAt` | date |  |
| `space.urls.app` | string |  |
| `space.urls.location` | string |  |
| `space.visibility` | string |  |
| `title` | string |  |

## Native endpoint

Through the native GitBook API, this operation is `GET /orgs/:organizationId/sites/:siteId/site-spaces` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-site-spaces.md) for the provider-specific parameters and requirements.

