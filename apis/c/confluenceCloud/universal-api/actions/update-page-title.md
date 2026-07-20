# Confluence: Update Page Title

Updates an existing page title in Confluence.

```
PUT https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/update-page-title
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/update-page-title" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloudId": "string",
  "id": "string",
  "title": "string",
  "version.number": 1,
  "status": "current"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/update-page-title', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloudId": "string",
    "id": "string",
    "title": "string",
    "version.number": 1,
    "status": "current"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cloudId` | string | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | string | yes | ID of the Confluence page. |
| `title` | string | yes | New title for the page. |
| `version.number` | number | yes | Incremented page version required when updating a page title. |
| `status` | string | yes | Current page status required by Confluence when updating a page title, usually current. Default: `current`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "body": {},
      "createdAt": "string",
      "id": "string",
      "lastOwnerId": {},
      "Links": {
        "base": "https://example.com",
        "editui": "https://example.com",
        "edituiv2": "https://example.com",
        "tinyui": "https://example.com",
        "webui": "https://example.com"
      },
      "ownerId": {},
      "parentId": {},
      "parentType": {},
      "position": 1,
      "spaceId": "string",
      "status": "string",
      "title": "string",
      "version": {
        "authorId": "string",
        "createdAt": "string",
        "message": {},
        "minorEdit": true,
        "ncsStepVersion": "string",
        "number": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `body` | object |  |
| `createdAt` | string |  |
| `id` | string |  |
| `lastOwnerId` | object |  |
| `Links.base` | string |  |
| `Links.editui` | string |  |
| `Links.edituiv2` | string |  |
| `Links.tinyui` | string |  |
| `Links.webui` | string |  |
| `ownerId` | object |  |
| `parentId` | object |  |
| `parentType` | object |  |
| `position` | number |  |
| `spaceId` | string |  |
| `status` | string |  |
| `title` | string |  |
| `version.authorId` | string |  |
| `version.createdAt` | string |  |
| `version.message` | object |  |
| `version.minorEdit` | boolean |  |
| `version.ncsStepVersion` | string |  |
| `version.number` | number |  |

## Native endpoint

Through the native Confluence API, this operation is `PUT /ex/confluence/:cloudId/wiki/api/v2/pages/:id/title` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page-title.md) for the provider-specific parameters and requirements.

