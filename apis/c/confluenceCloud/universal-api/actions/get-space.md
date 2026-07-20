# Confluence: Get Space

Retrieves an existing space from Confluence.

```
GET https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/get-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/get-space?connectionId=$CONNECTION_ID&cloudId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cloudId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/get-space?${params}`, {
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
| `cloudId` | string | yes | Confluence site cloud ID. Run List Accessible Resources to find it. |
| `id` | string | yes | ID of the Confluence space. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "createdAt": "string",
      "currentActiveAlias": "string",
      "homepageId": "string",
      "icon": {},
      "id": "string",
      "key": "string",
      "Links": {
        "base": "https://example.com",
        "webui": "https://example.com"
      },
      "name": "Ava Chen",
      "spaceOwnerId": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `createdAt` | string |  |
| `currentActiveAlias` | string |  |
| `homepageId` | string |  |
| `icon` | object |  |
| `id` | string |  |
| `key` | string |  |
| `Links.base` | string |  |
| `Links.webui` | string |  |
| `name` | string |  |
| `spaceOwnerId` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Confluence API, this operation is `GET /ex/confluence/:cloudId/wiki/api/v2/spaces/:id` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-space.md) for the provider-specific parameters and requirements.

