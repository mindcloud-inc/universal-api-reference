# Xperiencify: Remove Tag

Deletes tags from Xperiencify.

```
DELETE https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/remove-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xperiencify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/remove-tag?connectionId=$CONNECTION_ID&tagNames=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagNames": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xperiencify/latest/actions/remove-tag?${params}`, {
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
| `tags[]` | array<string> | Tag names returned by the delete endpoint. |

## Native endpoint

Through the native Xperiencify API, this operation is `DELETE /api/public/coach/tag/` (base URL `https://api.xperiencify.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tag.md) for the provider-specific parameters and requirements.

