# Gusto: Get Token Info

Retrieves OAuth token information from Gusto.

```
GET https://connect.mindcloud.co/v1/universal/gusto/latest/actions/get-token-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gusto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gusto/latest/actions/get-token-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gusto/latest/actions/get-token-info?${params}`, {
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
      "resource": {
        "type": "string",
        "uuid": "string"
      },
      "resourceOwner": {
        "type": "string",
        "uuid": "string"
      },
      "scope": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resource.type` | string |  |
| `resource.uuid` | string |  |
| `resourceOwner.type` | string |  |
| `resourceOwner.uuid` | string |  |
| `scope` | string |  |

## Native endpoint

Through the native Gusto API, this operation is `GET /v1/token_info` (base URL `https://api.gusto-demo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-info.md) for the provider-specific parameters and requirements.

