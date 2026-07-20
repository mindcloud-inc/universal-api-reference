# Matomo: Get Search Categories



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/actions-get-site-search-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/actions-get-site-search-categories?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/actions-get-site-search-categories?${params}`, {
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
      "exit_rate": 1,
      "label": "string",
      "nb_pages_per_search": 1,
      "nb_visits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exit_rate` | number | Matomo metric exit_rate |
| `label` | string | Search Category |
| `nb_pages_per_search` | number | Matomo metric nb_pages_per_search |
| `nb_visits` | number | Matomo metric nb_visits |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/actions-get-site-search-categories.md) for the provider-specific parameters and requirements.

