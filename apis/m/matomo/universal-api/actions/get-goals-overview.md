# Matomo: Get Goals Overview



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/get-goals-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/get-goals-overview?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/get-goals-overview?${params}`, {
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
| `idSite` | number | yes | Matomo API parameter. Default: `1`. |
| `period` | string | yes | Matomo API parameter. Default: `day`. |
| `date` | string | yes | Matomo API parameter. Default: `yesterday`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `segment` | string | no | Matomo API parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avg_order_revenue": 1,
      "conversion_rate": 1,
      "nb_conversions": 1,
      "nb_visits_converted": 1,
      "revenue": 1,
      "revenue_discount": 1,
      "revenue_shipping": 1,
      "revenue_subtotal": 1,
      "revenue_tax": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avg_order_revenue` | number | Matomo metric avg_order_revenue |
| `conversion_rate` | number | Matomo metric conversion_rate |
| `nb_conversions` | number | Matomo metric nb_conversions |
| `nb_visits_converted` | number | Matomo metric nb_visits_converted |
| `revenue` | number | Matomo metric revenue |
| `revenue_discount` | number | Matomo metric revenue_discount |
| `revenue_shipping` | number | Matomo metric revenue_shipping |
| `revenue_subtotal` | number | Matomo metric revenue_subtotal |
| `revenue_tax` | number | Matomo metric revenue_tax |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-goals-overview.md) for the provider-specific parameters and requirements.

