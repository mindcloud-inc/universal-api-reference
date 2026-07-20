# IgniSign: List Signature Requests



```
GET https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/list-signature-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgniSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/list-signature-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/list-signature-requests?${params}`, {
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
      "paginationData": {
        "nbEventsPerPage": 1,
        "page": 1,
        "total": 1
      },
      "signatureRequests": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paginationData.nbEventsPerPage` | number |  |
| `paginationData.page` | number |  |
| `paginationData.total` | number |  |
| `signatureRequests` | array<object> |  |

## Native endpoint

Through the native IgniSign API, this operation is `GET /v4/applications/:appId/envs/:appEnv/signature-requests` (base URL `https://api.ignisign.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signature-requests.md) for the provider-specific parameters and requirements.

