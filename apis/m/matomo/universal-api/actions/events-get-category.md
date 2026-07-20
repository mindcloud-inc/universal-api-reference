# Matomo: Get Event Categories



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/events-get-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/events-get-category?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/events-get-category?${params}`, {
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
      "avg_event_value": 1,
      "label": "string",
      "max_event_value": 1,
      "min_event_value": 1,
      "nb_events": 1,
      "nb_events_with_value": 1,
      "nb_uniq_visitors": 1,
      "nb_visits": 1,
      "sum_event_value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avg_event_value` | number | Matomo metric avg_event_value |
| `label` | string | Event Category |
| `max_event_value` | number | Matomo metric max_event_value |
| `min_event_value` | number | Matomo metric min_event_value |
| `nb_events` | number | Matomo metric nb_events |
| `nb_events_with_value` | number | Matomo metric nb_events_with_value |
| `nb_uniq_visitors` | number | Matomo metric nb_uniq_visitors |
| `nb_visits` | number | Matomo metric nb_visits |
| `sum_event_value` | number | Matomo metric sum_event_value |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/events-get-category.md) for the provider-specific parameters and requirements.

