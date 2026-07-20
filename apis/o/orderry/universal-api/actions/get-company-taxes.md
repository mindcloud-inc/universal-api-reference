# Orderry: Get Company Taxes

Retrieves company tax rates from Orderry.

```
GET https://connect.mindcloud.co/v1/universal/orderry/latest/actions/get-company-taxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orderry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderry/latest/actions/get-company-taxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderry/latest/actions/get-company-taxes?${params}`, {
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
      "id": 1,
      "is_enabled": true,
      "name": "Ava Chen",
      "rate": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `is_enabled` | boolean |  |
| `name` | string |  |
| `rate` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Orderry API, this operation is `GET settings/taxes` (base URL `https://api.orderry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-taxes.md) for the provider-specific parameters and requirements.

