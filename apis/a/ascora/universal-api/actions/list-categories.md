# Ascora: List Categories

Retrieves categories from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-categories?${params}`, {
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
| `filterText` | string | no | Search across the category name. |
| `parentOnly` | boolean | no | Return top-level categories only. |
| `categoryNumber` | number | no | Filter to category group 1 or 2. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ],
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Matching category records. |
| `success` | boolean | Whether Ascora returned the category search successfully. |
| `totalPages` | number | Total result pages returned by Ascora. |
| `totalRecords` | number | Total matching categories. |

## Native endpoint

Through the native Ascora API, this operation is `GET /Inventory/Categories` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

