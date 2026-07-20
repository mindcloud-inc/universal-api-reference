# Swipe One: List Tags



```
GET https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/list-tags?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/list-tags?${params}`, {
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
| `workspaceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "count": 1,
        "tags": [
          {
            "color": "string",
            "createdBy": {
              "id": "string",
              "name": "Ava Chen",
              "type": "string"
            },
            "Id": "string",
            "label": "string",
            "name": "Ava Chen",
            "V": 1,
            "workspaceId": "string"
          }
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.count` | number |  |
| `data.tags[].color` | string |  |
| `data.tags[].createdBy.id` | string |  |
| `data.tags[].createdBy.name` | string |  |
| `data.tags[].createdBy.type` | string |  |
| `data.tags[].Id` | string |  |
| `data.tags[].label` | string |  |
| `data.tags[].name` | string |  |
| `data.tags[].V` | number |  |
| `data.tags[].workspaceId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `GET /workspaces/:workspaceId/tags` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

