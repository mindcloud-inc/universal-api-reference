# CometAPI: List Files



```
GET https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/list-files-restored
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/list-files-restored?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/list-files-restored?${params}`, {
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
      "data": [
        {
          "createdAt": 1,
          "filename": "Ava Chen",
          "id": "string",
          "object": "string",
          "purpose": "string"
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
| `data[].createdAt` | number |  |
| `data[].filename` | string |  |
| `data[].id` | string |  |
| `data[].object` | string |  |
| `data[].purpose` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `GET /v1/files` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-files-restored.md) for the provider-specific parameters and requirements.

