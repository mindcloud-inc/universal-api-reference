# data.world: Get File Description and Labels

Retrieves file descriptions and labels from data.world.

```
GET https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/get-file-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a data.world `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/get-file-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/get-file-metadata?${params}`, {
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
      "description": "string",
      "file": "string",
      "labels": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `file` | string |  |
| `labels[]` | string |  |

## Native endpoint

Through the native data.world API, this operation is `GET /datasets/{owner}/{id}/files/{file}/metadata` (base URL `https://api.data.world/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-metadata.md) for the provider-specific parameters and requirements.

