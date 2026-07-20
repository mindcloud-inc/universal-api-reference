# Matomo: Get Content Piece



```
GET https://connect.mindcloud.co/v1/universal/matomo/latest/actions/contents-get-content-pieces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Matomo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/matomo/latest/actions/contents-get-content-pieces?connectionId=$CONNECTION_ID&idSite=1&period=day&date=yesterday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idSite": "1",
  "period": "day",
  "date": "yesterday"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/matomo/latest/actions/contents-get-content-pieces?${params}`, {
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
      "interaction_rate": 1,
      "label": "string",
      "nb_impressions": 1,
      "nb_interactions": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `interaction_rate` | number | Matomo metric interaction_rate |
| `label` | string | Content Piece |
| `nb_impressions` | number | Matomo metric nb_impressions |
| `nb_interactions` | number | Matomo metric nb_interactions |

## Native endpoint

Through the native Matomo API, this operation is `POST /index.php` (base URL `https://mindcloud.matomo.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/contents-get-content-pieces.md) for the provider-specific parameters and requirements.

