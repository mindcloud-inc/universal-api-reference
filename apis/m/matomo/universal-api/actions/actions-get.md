# Matomo: Get Actions - Main metrics



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/actions-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/actions-get?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/actions-get?${params}`, {
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
      "hits": 1,
      "nb_downloads": 1,
      "nb_keywords": 1,
      "nb_outlinks": 1,
      "nb_pageviews": 1,
      "nb_searches": 1,
      "nb_uniq_downloads": 1,
      "nb_uniq_outlinks": 1,
      "nb_uniq_pageviews": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avg_time_generation` | number | Matomo metric avg_time_generation |
| `hits` | number | Matomo metric hits |
| `nb_downloads` | number | Matomo metric nb_downloads |
| `nb_keywords` | number | Matomo metric nb_keywords |
| `nb_outlinks` | number | Matomo metric nb_outlinks |
| `nb_pageviews` | number | Matomo metric nb_pageviews |
| `nb_searches` | number | Matomo metric nb_searches |
| `nb_uniq_downloads` | number | Matomo metric nb_uniq_downloads |
| `nb_uniq_outlinks` | number | Matomo metric nb_uniq_outlinks |
| `nb_uniq_pageviews` | number | Matomo metric nb_uniq_pageviews |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/actions-get.md) for the provider-specific parameters and requirements.

