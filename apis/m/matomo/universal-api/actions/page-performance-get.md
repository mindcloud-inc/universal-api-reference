# Matomo: Get Performance overview



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/page-performance-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/page-performance-get?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/page-performance-get?${params}`, {
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
      "avg_page_load_time": 1,
      "avg_time_dom_completion": 1,
      "avg_time_dom_processing": 1,
      "avg_time_network": 1,
      "avg_time_on_load": 1,
      "avg_time_server": 1,
      "avg_time_transfer": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avg_page_load_time` | number | Matomo metric avg_page_load_time |
| `avg_time_dom_completion` | number | Matomo metric avg_time_dom_completion |
| `avg_time_dom_processing` | number | Matomo metric avg_time_dom_processing |
| `avg_time_network` | number | Matomo metric avg_time_network |
| `avg_time_on_load` | number | Matomo metric avg_time_on_load |
| `avg_time_server` | number | Matomo metric avg_time_server |
| `avg_time_transfer` | number | Matomo metric avg_time_transfer |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/page-performance-get.md) for the provider-specific parameters and requirements.

