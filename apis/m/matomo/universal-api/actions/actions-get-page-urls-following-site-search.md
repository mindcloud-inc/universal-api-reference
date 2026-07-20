# Matomo: Get Pages Following a Site Search



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/actions-get-page-urls-following-site-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/actions-get-page-urls-following-site-search?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/actions-get-page-urls-following-site-search?${params}`, {
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
      "avg_time_generation": 1,
      "avg_time_on_page": 1,
      "bounce_rate": 1,
      "exit_rate": 1,
      "label": "string",
      "nb_hits": 1,
      "nb_hits_following_search": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avg_time_generation` | number | Matomo metric avg_time_generation |
| `avg_time_on_page` | number | Matomo metric avg_time_on_page |
| `bounce_rate` | number | Matomo metric bounce_rate |
| `exit_rate` | number | Matomo metric exit_rate |
| `label` | string | Destination Page |
| `nb_hits` | number | Matomo metric nb_hits |
| `nb_hits_following_search` | number | Matomo metric nb_hits_following_search |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/actions-get-page-urls-following-site-search.md) for the provider-specific parameters and requirements.

