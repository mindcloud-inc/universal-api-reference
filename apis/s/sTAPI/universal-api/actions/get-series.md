# STAPI: Get Series



```
GET https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-series?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTAPI/latest/actions/get-series?${params}`, {
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
| `uid` | string | yes | Series unique ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "series": {
        "abbreviation": "string",
        "episodesCount": 1,
        "productionEndYear": 1,
        "productionStartYear": 1,
        "title": "string",
        "uid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `series` | object |  |
| `series.abbreviation` | string |  |
| `series.episodesCount` | number |  |
| `series.productionEndYear` | number |  |
| `series.productionStartYear` | number |  |
| `series.title` | string |  |
| `series.uid` | string |  |

## Native endpoint

Through the native STAPI API, this operation is `GET /v1/rest/series` (base URL `https://stapi.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-series.md) for the provider-specific parameters and requirements.

