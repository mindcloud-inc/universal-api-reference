# Matomo: Get All Websites dashboard



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/multi-sites-get-all
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/multi-sites-get-all?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/multi-sites-get-all?${params}`, {
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
      "actions_evolution": 1,
      "ai_chatbots_requests": 1,
      "ai_chatbots_requests_evolution": 1,
      "ecommerce_revenue": 1,
      "ecommerce_revenue_evolution": 1,
      "hits": 1,
      "hits_evolution": 1,
      "label": "string",
      "nb_actions": 1,
      "nb_conversions": 1,
      "nb_conversions_evolution": 1,
      "nb_pageviews": 1,
      "nb_visits": 1,
      "orders": 1,
      "orders_evolution": 1,
      "pageviews_evolution": 1,
      "revenue": 1,
      "revenue_evolution": 1,
      "visits_evolution": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions_evolution` | number | Matomo metric actions_evolution |
| `ai_chatbots_requests` | number | Matomo metric ai_chatbots_requests |
| `ai_chatbots_requests_evolution` | number | Matomo metric ai_chatbots_requests_evolution |
| `ecommerce_revenue` | number | Matomo metric ecommerce_revenue |
| `ecommerce_revenue_evolution` | number | Matomo metric ecommerce_revenue_evolution |
| `hits` | number | Matomo metric hits |
| `hits_evolution` | number | Matomo metric hits_evolution |
| `label` | string | Website |
| `nb_actions` | number | Matomo metric nb_actions |
| `nb_conversions` | number | Matomo metric nb_conversions |
| `nb_conversions_evolution` | number | Matomo metric nb_conversions_evolution |
| `nb_pageviews` | number | Matomo metric nb_pageviews |
| `nb_visits` | number | Matomo metric nb_visits |
| `orders` | number | Matomo metric orders |
| `orders_evolution` | number | Matomo metric orders_evolution |
| `pageviews_evolution` | number | Matomo metric pageviews_evolution |
| `revenue` | number | Matomo metric revenue |
| `revenue_evolution` | number | Matomo metric revenue_evolution |
| `visits_evolution` | number | Matomo metric visits_evolution |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/multi-sites-get-all.md) for the provider-specific parameters and requirements.

