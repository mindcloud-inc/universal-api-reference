# Edoobox: List Vats

Retrieves a list of VAT rates from Edoobox.

```
GET https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/list-vats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edoobox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/list-vats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/list-vats?${params}`, {
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
      "b2b": true,
      "country": "string",
      "default": true,
      "description": "string",
      "id": "string",
      "lastChange": "2026-05-07T12:00:00.000Z",
      "status": true,
      "vatNumber": "string",
      "vatPercent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `b2b` | boolean |  |
| `country` | string |  |
| `default` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `lastChange` | date |  |
| `status` | boolean |  |
| `vatNumber` | string |  |
| `vatPercent` | number |  |

## Native endpoint

Through the native Edoobox API, this operation is `GET /vat/list` (base URL `https://app2.edoobox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vats.md) for the provider-specific parameters and requirements.

