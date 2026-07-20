# lc.cx: Update Link

Updates an existing short link in lc.cx.

```
PUT https://connect.mindcloud.co/v1/universal/lccx/latest/actions/update-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lc.cx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lccx/latest/actions/update-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "linkId": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lccx/latest/actions/update-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "linkId": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `linkId` | string | yes | The ID of the link to update. |
| `rfcValidation` | boolean | no | Whether to validate the destination URL against the RFC format. |
| `tldValidation` | boolean | no | Whether to validate the destination URL top-level domain. |
| `destination` | string | no | The new destination URL for the shortlink. |
| `tagIds[]` | array<string> | no | Tag IDs to attach to the shortlink. Use an empty array to remove all tags. |
| `note` | string | no | An optional note for the shortlink. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native lc.cx API returns.

## Native endpoint

Through the native lc.cx API, this operation is `PATCH /links/update/:id` (base URL `https://api.lc.cx/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-link.md) for the provider-specific parameters and requirements.

