# Mews: Get All Accounting Categories

Retrieves accounting categories from Mews.

```
GET https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-accounting-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mews `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-accounting-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mews/latest/actions/get-all-accounting-categories?${params}`, {
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
      "code": "string",
      "externalCode": "string",
      "id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "updatedUtc": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Accounting category code. |
| `externalCode` | string | External accounting code when present. |
| `id` | string | Unique identifier of the accounting category. |
| `isActive` | boolean | Whether the accounting category is active. |
| `name` | string | Accounting category name. |
| `updatedUtc` | date | Last update timestamp in UTC. |

## Native endpoint

Through the native Mews API, this operation is `POST /accountingCategories/getAll` (base URL `{{credentials.platformAddress}}/api/connector/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-accounting-categories.md) for the provider-specific parameters and requirements.

