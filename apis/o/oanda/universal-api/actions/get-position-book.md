# Oanda: Get Position Book

Retrieves position book snapshots from Oanda.

```
GET https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-position-book
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oanda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-position-book?connectionId=$CONNECTION_ID&instrument=EUR_USD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "instrument": "EUR_USD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oanda/latest/actions/get-position-book?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | no | The time of the snapshot to fetch. |
| `instrument` | string | yes | Instrument name, for example EUR_USD. Default: `EUR_USD`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "positionBook": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `positionBook` | object | Position book snapshot including buckets. |

## Native endpoint

Through the native Oanda API, this operation is `GET /v3/instruments/:instrument/positionBook` (base URL `https://exchange-rates-api.oanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-position-book.md) for the provider-specific parameters and requirements.

