# IronWiFi: List Attributes

Retrieves attributes for a specific table from IronWiFi.

```
GET https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/list-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IronWiFi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/list-attributes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironWiFi/latest/actions/list-attributes?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Attribute payload returned by IronWiFi. This endpoint may return an empty string when no attributes match the requested table. |

## Native endpoint

Through the native IronWiFi API, this operation is `GET /attributes` (base URL `https://console.ironwifi.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attributes.md) for the provider-specific parameters and requirements.

