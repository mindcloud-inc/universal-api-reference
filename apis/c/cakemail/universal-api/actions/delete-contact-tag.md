# Cakemail: Delete Contact Tag

Deletes a contact tag from Cakemail.

```
DELETE https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/delete-contact-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cakemail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/delete-contact-tag?connectionId=$CONNECTION_ID&tag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/delete-contact-tag?${params}`, {
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
| `tag` | string | yes | Contact tag name to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cakemail API returns.

## Native endpoint

Through the native Cakemail API, this operation is `DELETE /tags/:tag` (base URL `https://api.cakemail.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-tag.md) for the provider-specific parameters and requirements.

