# Becon: List Currencies

Retrieves available currencies and chains from Becon.

```
GET https://connect.mindcloud.co/v1/universal/becon/latest/actions/list-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Becon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/becon/latest/actions/list-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/becon/latest/actions/list-currencies?${params}`, {
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
      "chain": "string",
      "id": 1,
      "iso_name": "Ava Chen",
      "logo": "string",
      "name": "Ava Chen",
      "network": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chain` | string | Blockchain network name. |
| `id` | number | Currency identifier. |
| `iso_name` | string | Currency ISO name. |
| `logo` | string | Currency logo URL. |
| `name` | string | Currency display name. |
| `network` | string | Token network variant when applicable. |

## Native endpoint

Through the native Becon API, this operation is `GET /v1/currencies` (base URL `https://external-api.bcon.global/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-currencies.md) for the provider-specific parameters and requirements.

