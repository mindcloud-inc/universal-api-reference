# CleverReach: Get Attribute Limits

Retrieves account attribute limits from CleverReach.

```
GET https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/get-attribute-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CleverReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/get-attribute-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cleverReach/latest/actions/get-attribute-limits?${params}`, {
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
      "available": 1,
      "canCreate": true,
      "max": "string",
      "used": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | number |  |
| `canCreate` | boolean |  |
| `max` | string |  |
| `used` | number |  |

## Native endpoint

Through the native CleverReach API, this operation is `GET /v3/attributes/limits.json` (base URL `https://rest.cleverreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attribute-limits.md) for the provider-specific parameters and requirements.

