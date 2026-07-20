# Convex: Get Token Details

Retrieves details about the current Convex token.

```
GET https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-token-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convex/latest/actions/get-token-details?${params}`, {
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
      "createTime": 1,
      "name": "Ava Chen",
      "teamId": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | number |  |
| `name` | string |  |
| `teamId` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Convex API, this operation is `GET /token_details` (base URL `https://api.convex.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-details.md) for the provider-specific parameters and requirements.

