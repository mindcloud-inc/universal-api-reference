# Reloadify: Create Or Update Review

Creates or updates a review in Reloadify.

```
PUT https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageId": "string",
  "review.id": "string",
  "review.product_id": "string",
  "review.profile_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-or-update-review', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageId": "string",
    "review.id": "string",
    "review.product_id": "string",
    "review.profile_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageId` | string | yes | Reloadify language ID. |
| `review.id` | string | yes | Review identifier. |
| `review.product_id` | string | yes | Existing product ID. |
| `review.profile_id` | string | yes | Existing profile ID. |

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

Through the native Reloadify API, this operation is `PUT /v2/languages/:language_id/reviews` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-review.md) for the provider-specific parameters and requirements.

