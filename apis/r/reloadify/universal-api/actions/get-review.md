# Reloadify: Get Review

Retrieves a review from Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-review?connectionId=$CONNECTION_ID&languageId=string&reviewId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "languageId": "string",
  "reviewId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-review?${params}`, {
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
| `languageId` | string | yes | Reloadify language ID. |
| `reviewId` | string | yes | Review identifier. |

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

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/reviews/:review_id` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-review.md) for the provider-specific parameters and requirements.

