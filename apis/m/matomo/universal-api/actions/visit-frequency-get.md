# Matomo: Get Returning Visits



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/visit-frequency-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/visit-frequency-get?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/visit-frequency-get?${params}`, {
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
      "avg_time_on_site_new": 1,
      "avg_time_on_site_returning": 1,
      "bounce_rate_new": 1,
      "bounce_rate_returning": 1,
      "max_actions_new": 1,
      "max_actions_returning": 1,
      "nb_actions_new": 1,
      "nb_actions_per_visit_new": 1,
      "nb_actions_per_visit_returning": 1,
      "nb_actions_returning": 1,
      "nb_uniq_visitors_new": 1,
      "nb_uniq_visitors_returning": 1,
      "nb_users_new": 1,
      "nb_users_returning": 1,
      "nb_visits_new": 1,
      "nb_visits_returning": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avg_time_on_site_new` | number | Matomo metric avg_time_on_site_new |
| `avg_time_on_site_returning` | number | Matomo metric avg_time_on_site_returning |
| `bounce_rate_new` | number | Matomo metric bounce_rate_new |
| `bounce_rate_returning` | number | Matomo metric bounce_rate_returning |
| `max_actions_new` | number | Matomo metric max_actions_new |
| `max_actions_returning` | number | Matomo metric max_actions_returning |
| `nb_actions_new` | number | Matomo metric nb_actions_new |
| `nb_actions_per_visit_new` | number | Matomo metric nb_actions_per_visit_new |
| `nb_actions_per_visit_returning` | number | Matomo metric nb_actions_per_visit_returning |
| `nb_actions_returning` | number | Matomo metric nb_actions_returning |
| `nb_uniq_visitors_new` | number | Matomo metric nb_uniq_visitors_new |
| `nb_uniq_visitors_returning` | number | Matomo metric nb_uniq_visitors_returning |
| `nb_users_new` | number | Matomo metric nb_users_new |
| `nb_users_returning` | number | Matomo metric nb_users_returning |
| `nb_visits_new` | number | Matomo metric nb_visits_new |
| `nb_visits_returning` | number | Matomo metric nb_visits_returning |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/visit-frequency-get.md) for the provider-specific parameters and requirements.

