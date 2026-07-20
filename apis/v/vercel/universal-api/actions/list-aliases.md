# Vercel: List Aliases

Retrieves all alias records from Vercel.

```
GET https://connect.mindcloud.co/v1/universal/vercel/latest/actions/list-aliases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/list-aliases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/list-aliases?${params}`, {
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
      "alias": "string",
      "createdAt": 1,
      "deploymentId": "string",
      "projectId": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `createdAt` | number |  |
| `deploymentId` | string |  |
| `projectId` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Vercel API, this operation is `GET /v4/aliases` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-aliases.md) for the provider-specific parameters and requirements.

