# Matomo: Get Device brand



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/devices-detection-get-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/devices-detection-get-brand?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/devices-detection-get-brand?${params}`, {
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
      "avg_time_on_site": 1,
      "bounce_rate": 1,
      "conversion_rate": 1,
      "label": "string",
      "nb_actions": 1,
      "nb_actions_per_visit": 1,
      "nb_conversions": 1,
      "nb_uniq_visitors": 1,
      "nb_users": 1,
      "nb_visits": 1,
      "revenue": 1,
      "revenue_per_visit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avg_time_on_site` | number | Matomo metric avg_time_on_site |
| `bounce_rate` | number | Matomo metric bounce_rate |
| `conversion_rate` | number | Matomo metric conversion_rate |
| `label` | string | Device brand |
| `nb_actions` | number | Matomo metric nb_actions |
| `nb_actions_per_visit` | number | Matomo metric nb_actions_per_visit |
| `nb_conversions` | number | Matomo metric nb_conversions |
| `nb_uniq_visitors` | number | Matomo metric nb_uniq_visitors |
| `nb_users` | number | Matomo metric nb_users |
| `nb_visits` | number | Matomo metric nb_visits |
| `revenue` | number | Matomo metric revenue |
| `revenue_per_visit` | number | Matomo metric revenue_per_visit |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/devices-detection-get-brand.md) for the provider-specific parameters and requirements.

