# Tiliter: Health Check

Retrieves the Tiliter Recognition API health status.

```
GET https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/health-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/health-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/health-check?${params}`, {
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
      "authenticatedCustomerId": {
        "dependency": {},
        "useCache": true
      },
      "it's": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticatedCustomerId` | object |  |
| `authenticatedCustomerId.dependency` | object |  |
| `authenticatedCustomerId.useCache` | boolean |  |
| `it's` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `GET /` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/health-check.md) for the provider-specific parameters and requirements.

