# Loyverse: Delete Category

Deletes an existing category from Loyverse.

```
DELETE https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/delete-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/delete-category?connectionId=$CONNECTION_ID&categoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/delete-category?${params}`, {
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
| `categoryId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedObjectIds": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedObjectIds` | array<string> | The list of deleted object ids |

## Native endpoint

Through the native Loyverse API, this operation is `DELETE /categories/:category_id` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-category.md) for the provider-specific parameters and requirements.

