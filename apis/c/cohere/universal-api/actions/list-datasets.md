# Cohere: List Datasets

Lists available training datasets in Cohere.

```
GET https://connect.mindcloud.co/v1/universal/cohere/latest/actions/list-datasets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cohere `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cohere/latest/actions/list-datasets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cohere/latest/actions/list-datasets?${params}`, {
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
      "datasets": [
        {}
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datasets` | array<object> |  |
| `nextPageToken` | string |  |

## Native endpoint

Through the native Cohere API, this operation is `GET /v1/datasets` (base URL `https://api.cohere.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datasets.md) for the provider-specific parameters and requirements.

