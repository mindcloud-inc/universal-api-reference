# UniOne: Delete Template

Deletes an email template from UniOne by ID.

```
DELETE https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/delete-template?connectionId=$CONNECTION_ID&id=cc6b94dc-2ebc-11f1-a0f4-8a7db48392b4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "cc6b94dc-2ebc-11f1-a0f4-8a7db48392b4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/delete-template?${params}`, {
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
| `id` | string | yes | Template identifier to delete. Example: `cc6b94dc-2ebc-11f1-a0f4-8a7db48392b4`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UniOne API returns.

## Native endpoint

Through the native UniOne API, this operation is `POST template/delete.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

