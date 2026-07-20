# Hiboutik: List Categories

Retrieves product categories from Hiboutik.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-categories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryBckColor": "string",
      "categoryColor": "string",
      "categoryEnabled": 1,
      "categoryId": 1,
      "categoryIdParent": 1,
      "categoryName": "Ava Chen",
      "categoryPosition": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryBckColor` | string |  |
| `categoryColor` | string |  |
| `categoryEnabled` | number |  |
| `categoryId` | number |  |
| `categoryIdParent` | number |  |
| `categoryName` | string |  |
| `categoryPosition` | number |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /categories` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

