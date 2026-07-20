# Sponsy: Delete Tag

Deletes a tag from Sponsy.

```
DELETE https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/delete-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/delete-tag?connectionId=$CONNECTION_ID&tagId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/delete-tag?${params}`, {
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
| `tagId` | string | yes | Tag ID from Sponsy. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sponsy API returns.

## Native endpoint

Through the native Sponsy API, this operation is `DELETE /v1/tags/:tagId` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tag.md) for the provider-specific parameters and requirements.

