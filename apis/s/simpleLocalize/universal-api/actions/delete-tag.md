# SimpleLocalize: Delete Tag

Deletes an existing tag from SimpleLocalize.

```
DELETE https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/delete-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/delete-tag?connectionId=$CONNECTION_ID&tagName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/delete-tag?${params}`, {
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
| `tagName` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SimpleLocalize API returns.

## Native endpoint

Through the native SimpleLocalize API, this operation is `DELETE /api/v1/tags/{tagName}` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tag.md) for the provider-specific parameters and requirements.

