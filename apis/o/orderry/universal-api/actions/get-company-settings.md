# Orderry: Get Company Settings



```
GET https://connect.mindcloud.co/v1/universal/orderry/latest/actions/get-company-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orderry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderry/latest/actions/get-company-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderry/latest/actions/get-company-settings?${params}`, {
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
      "success": true,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the request succeeded. |
| `timezone` | string | The company's configured timezone. |

## Native endpoint

Through the native Orderry API, this operation is `GET settings/company` (base URL `https://api.orderry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-settings.md) for the provider-specific parameters and requirements.

