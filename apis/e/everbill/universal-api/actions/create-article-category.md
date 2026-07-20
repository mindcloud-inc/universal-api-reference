# Everbill: Create Article Category

Creates a new article category in Everbill.

```
POST https://connect.mindcloud.co/v1/universal/everbill/latest/actions/create-article-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everbill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/everbill/latest/actions/create-article-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/everbill/latest/actions/create-article-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | name request body field. |
| `color` | string | no | color request body field. |
| `favorit` | boolean | no | favorit request body field. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parent_id` | number | no | parent_id request body field. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Everbill API returns.

## Native endpoint

Through the native Everbill API, this operation is `POST /article_categories/add` (base URL `https://api.everbill.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-article-category.md) for the provider-specific parameters and requirements.

