# Rownd Data Privacy: List OIDC Clients



```
GET https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/list-oidc-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/list-oidc-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/list-oidc-clients?${params}`, {
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
      "results": [
        {}
      ],
      "total_results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | OIDC client records returned by Rownd. |
| `total_results` | number | Total number of OIDC clients returned. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `GET /oidc-clients` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-oidc-clients.md) for the provider-specific parameters and requirements.

