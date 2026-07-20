# Abyssale: List Designs By Category

Retrieves designs from Abyssale by category.

```
GET https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/list-designs-by-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abyssale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/list-designs-by-category?connectionId=$CONNECTION_ID&category_id=%3Ccategory%20uuid%3E" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category_id": "<category uuid>"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/list-designs-by-category?${params}`, {
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
| `category_id` | string | yes | Unique identifier (UUID) of a category. Filter designs by a category. Example: `<category uuid>`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Abyssale API returns.

## Native endpoint

Through the native Abyssale API, this operation is `GET /designs` (base URL `https://api.abyssale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-designs-by-category.md) for the provider-specific parameters and requirements.

