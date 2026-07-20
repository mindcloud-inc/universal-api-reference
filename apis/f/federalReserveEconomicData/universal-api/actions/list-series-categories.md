# Federal Reserve Economic Data: List Series Categories

Retrieves categories for a series from Federal Reserve Economic Data.

```
GET https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-series-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Reserve Economic Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-series-categories?connectionId=$CONNECTION_ID&series_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "series_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/list-series-categories?${params}`, {
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
| `series_id` | string | yes | The id for a series. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {
          "id": 1,
          "name": "Ava Chen",
          "parent_id": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories[].id` | number |  |
| `categories[].name` | string |  |
| `categories[].parent_id` | number |  |

## Native endpoint

Through the native Federal Reserve Economic Data API, this operation is `GET /fred/series/categories` (base URL `https://api.stlouisfed.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-series-categories.md) for the provider-specific parameters and requirements.

