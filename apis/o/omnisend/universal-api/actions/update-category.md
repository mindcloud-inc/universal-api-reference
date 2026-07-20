# Omnisend: Update Category

Updates an existing product category in Omnisend.

```
PUT https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/update-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnisend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/update-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "categoryID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/update-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "categoryID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryID` | string | yes | Unique Omnisend category identifier. |
| `title` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Omnisend API returns.

## Native endpoint

Through the native Omnisend API, this operation is `PATCH /v5/product-categories/:categoryID` (base URL `https://api.omnisend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-category.md) for the provider-specific parameters and requirements.

