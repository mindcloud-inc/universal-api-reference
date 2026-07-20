# Crexendo: Get My Domain Info

Retrieves your domain info from Crexendo.

```
GET https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/get-my-domain-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crexendo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/get-my-domain-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/get-my-domain-info?${params}`, {
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
      "count-users-configured": 1,
      "description": "string",
      "domain": "string",
      "domain-type": "string",
      "reseller": "string",
      "time-zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count-users-configured` | number |  |
| `description` | string |  |
| `domain` | string |  |
| `domain-type` | string |  |
| `reseller` | string |  |
| `time-zone` | string |  |

## Native endpoint

Through the native Crexendo API, this operation is `GET /domains/~` (base URL `https://ns-api.com/ns-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-domain-info.md) for the provider-specific parameters and requirements.

