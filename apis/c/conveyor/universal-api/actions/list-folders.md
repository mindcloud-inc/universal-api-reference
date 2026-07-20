# Conveyor: List Folders

Retrieves folders from the Conveyor exchange.

```
GET https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-folders?${params}`, {
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
      "_embedded": {
        "folders": [
          {
            "id": "string",
            "name": "Ava Chen"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_embedded` | object |  |
| `_embedded.folders` | array<object> |  |
| `_embedded.folders[].id` | string |  |
| `_embedded.folders[].name` | string |  |

## Native endpoint

Through the native Conveyor API, this operation is `GET /v2/exchange/folders` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

