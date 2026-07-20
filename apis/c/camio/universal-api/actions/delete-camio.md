# Camio: Delete Camio

Deletes a Camio from Camio.

```
DELETE https://connect.mindcloud.co/v1/universal/camio/latest/actions/delete-camio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Camio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/camio/latest/actions/delete-camio?connectionId=$CONNECTION_ID&id=string&viewToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "viewToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/camio/latest/actions/delete-camio?${params}`, {
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
| `id` | string | yes | Observed runtime requires the Camio id alongside the view token for reliable deletion. |
| `viewToken` | string | yes | The Camio view token to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Camio API returns.

## Native endpoint

Through the native Camio API, this operation is `DELETE /users/me/camios` (base URL `https://camio.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-camio.md) for the provider-specific parameters and requirements.

