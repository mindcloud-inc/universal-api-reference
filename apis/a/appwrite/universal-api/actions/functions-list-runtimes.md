# Appwrite: List runtimes

Retrieves a list of runtimes from your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-list-runtimes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-list-runtimes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-list-runtimes?${params}`, {
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
      "runtimes": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `runtimes` | array<object> | List of runtimes. |
| `total` | number | Total number of runtimes that matched your query. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /functions/runtimes` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/functions-list-runtimes.md) for the provider-specific parameters and requirements.

