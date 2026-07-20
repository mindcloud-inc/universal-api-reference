# Federal Reserve Economic Data: Get Category

Retrieves a category from Federal Reserve Economic Data.

```
GET https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/get-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Reserve Economic Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/get-category?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/get-category?${params}`, {
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
| `category_id` | number | no | The id for a category. |

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

Through the native Federal Reserve Economic Data API, this operation is `GET /fred/category` (base URL `https://api.stlouisfed.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-category.md) for the provider-specific parameters and requirements.

