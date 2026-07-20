# Xperiencify: Add New Tag

Creates new tags in Xperiencify.

```
POST https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/add-new-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xperiencify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/add-new-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tagNames": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/add-new-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tagNames": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tagNames` | string | yes | One or more tag names separated by commas. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tags": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tags[]` | array<string> | Created tag names returned by the endpoint. |

## Native endpoint

Through the native Xperiencify API, this operation is `POST /api/public/coach/tag/` (base URL `https://api.xperiencify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-new-tag.md) for the provider-specific parameters and requirements.

