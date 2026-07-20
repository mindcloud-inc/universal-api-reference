# Notifyre SMS: List Fax Prices

Retrieves current fax prices from Notifyre.

```
GET https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/list-fax-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/list-fax-prices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/list-fax-prices?${params}`, {
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
      "prices": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `prices` | array<object> | Fax prices by country or prefix when returned by the API. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `GET /fax/send/prices` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fax-prices.md) for the provider-specific parameters and requirements.

