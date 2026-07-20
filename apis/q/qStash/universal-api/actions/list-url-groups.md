# QStash: List URL Groups

Retrieves all URL Groups from QStash.

```
GET https://connect.mindcloud.co/v1/universal/qStash/latest/actions/list-url-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/list-url-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qStash/latest/actions/list-url-groups?${params}`, {
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
      "createdAt": 1,
      "endpoints": [
        {}
      ],
      "forwardAllHeaders": true,
      "method": "string",
      "name": "Ava Chen",
      "retries": 1,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `endpoints` | array<object> |  |
| `forwardAllHeaders` | boolean |  |
| `method` | string |  |
| `name` | string |  |
| `retries` | number |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native QStash API, this operation is `GET /v2/topics` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-url-groups.md) for the provider-specific parameters and requirements.

