# GitBook: Add Space To Site

Adds an existing space to a GitBook site.

```
POST https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/add-space-to-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/add-space-to-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "siteId": "string",
  "spaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/add-space-to-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "siteId": "string",
    "spaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `draft` | boolean | no |  |
| `organizationId` | string | yes |  |
| `sectionId` | string | no |  |
| `siteId` | string | yes |  |
| `spaceId` | string | yes |  |

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

Through the native GitBook API, this operation is `POST /orgs/:organizationId/sites/:siteId/site-spaces` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-space-to-site.md) for the provider-specific parameters and requirements.

