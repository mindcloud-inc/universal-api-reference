# HappyFox: List Categories

Retrieves categories from HappyFox.

```
GET https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-categories?${params}`, {
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
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "prepopulateCc": "string",
      "public": true,
      "timeSpentMandatory": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Category description. |
| `id` | number | HappyFox category ID. |
| `name` | string | Category display name. |
| `prepopulateCc` | string | Default CC recipients configured for the category. |
| `public` | boolean | Whether the category is visible to end users. |
| `timeSpentMandatory` | boolean | Whether time entry is mandatory for tickets in this category. |

## Native endpoint

Through the native HappyFox API, this operation is `GET /categories/` (base URL `https://{{credentials.accountDomain}}/api/1.1/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

