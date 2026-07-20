# LinkTwin: Delete Domain

Deletes an existing branded domain from LinkTwin.

```
DELETE https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/delete-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/delete-domain?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/delete-domain?${params}`, {
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
| `id` | string | yes | Example: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LinkTwin API returns.

## Native endpoint

Through the native LinkTwin API, this operation is `DELETE /domain/:id/delete` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-domain.md) for the provider-specific parameters and requirements.

