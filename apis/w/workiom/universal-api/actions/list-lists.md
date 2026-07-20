# Workiom: List Lists

Retrieves lists from your Workiom workspace.

```
GET https://connect.mindcloud.co/v1/universal/workiom/latest/actions/list-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiom/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiom/latest/actions/list-lists?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "appId": "string",
          "creationTime": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "icon": "string",
          "id": "string",
          "isVisible": true,
          "lastModificationTime": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "type": "string",
          "visibility": "string"
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
| `items[].appId` | string |  |
| `items[].creationTime` | date |  |
| `items[].description` | string |  |
| `items[].icon` | string |  |
| `items[].id` | string |  |
| `items[].isVisible` | boolean |  |
| `items[].lastModificationTime` | date |  |
| `items[].name` | string |  |
| `items[].type` | string |  |
| `items[].visibility` | string |  |

## Native endpoint

Through the native Workiom API, this operation is `GET /api/services/app/Lists/GetAll` (base URL `https://api.workiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-lists.md) for the provider-specific parameters and requirements.

