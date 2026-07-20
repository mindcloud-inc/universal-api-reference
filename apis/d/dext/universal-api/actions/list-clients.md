# Dext: List Clients

Retrieves all accessible clients from Dext.

```
GET https://connect.mindcloud.co/v1/universal/dext/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dext `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dext/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dext/latest/actions/list-clients?${params}`, {
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
      "alertLevel": "string",
      "healthScore": 1,
      "id": "string",
      "name": "Ava Chen",
      "practiceCode": "string",
      "providerName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alertLevel` | string |  |
| `healthScore` | number |  |
| `id` | string |  |
| `name` | string |  |
| `practiceCode` | string |  |
| `providerName` | string |  |

## Native endpoint

Through the native Dext API, this operation is `GET /clients` (base URL `https://api.precision.dext.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

