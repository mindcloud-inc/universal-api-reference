# Reloadify: List Reviews

Retrieves reviews from Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-reviews?connectionId=$CONNECTION_ID&limit=25&offset=0&languageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "languageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/list-reviews?${params}`, {
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
| `created_after` | string | no | Only include reviews created after this timestamp. |
| `created_before` | string | no | Only include reviews created before this timestamp. |
| `languageId` | string | yes | Reloadify language ID. |
| `updated_after` | string | no | Only include reviews updated after this timestamp. |
| `updated_before` | string | no | Only include reviews updated before this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "custom_attributes": [
        {}
      ],
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "product_id": "string",
      "profile_id": "string",
      "score": 1,
      "updated_at": "string",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `custom_attributes` | array<object> |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `product_id` | string |  |
| `profile_id` | string |  |
| `score` | number |  |
| `updated_at` | string |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/reviews` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reviews.md) for the provider-specific parameters and requirements.

