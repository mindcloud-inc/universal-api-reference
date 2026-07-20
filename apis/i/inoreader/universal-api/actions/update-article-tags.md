# Inoreader: Update Article Tags

Updates article tags in Inoreader.

```
PUT https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/update-article-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inoreader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/update-article-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemIds": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/update-article-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemIds": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemIds` | string | yes | One or more article IDs to update. Accepts multiple values as an array. |
| `addTag` | string | no | System or custom tag to add to the item. |
| `removeTag` | string | no | System or custom tag to remove from the item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Provider acknowledgement returned by Inoreader for the edit-tag mutation. |

## Native endpoint

Through the native Inoreader API, this operation is `POST /edit-tag` (base URL `https://www.inoreader.com/reader/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-article-tags.md) for the provider-specific parameters and requirements.

