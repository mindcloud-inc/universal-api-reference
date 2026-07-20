# Confluence: List Spaces

Retrieves a list of spaces from Confluence.

```
GET https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-spaces?connectionId=$CONNECTION_ID&limit=25&offset=0&cloudId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "cloudId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-spaces?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "Links": {
        "base": "https://example.com"
      },
      "results": [
        {
          "authorId": "string",
          "createdAt": "string",
          "currentActiveAlias": "string",
          "description": {},
          "homepageId": "string",
          "icon": {},
          "id": "string",
          "key": "string",
          "Links": {
            "webui": "https://example.com"
          },
          "name": "Ava Chen",
          "spaceOwnerId": "string",
          "status": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Links.base` | string |  |
| `results[].authorId` | string |  |
| `results[].createdAt` | string |  |
| `results[].currentActiveAlias` | string |  |
| `results[].description` | object |  |
| `results[].homepageId` | string |  |
| `results[].icon` | object |  |
| `results[].id` | string |  |
| `results[].key` | string |  |
| `results[].Links.webui` | string |  |
| `results[].name` | string |  |
| `results[].spaceOwnerId` | string |  |
| `results[].status` | string |  |
| `results[].type` | string |  |

## Native endpoint

Through the native Confluence API, this operation is `GET /ex/confluence/:cloudId/wiki/api/v2/spaces` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-spaces.md) for the provider-specific parameters and requirements.

