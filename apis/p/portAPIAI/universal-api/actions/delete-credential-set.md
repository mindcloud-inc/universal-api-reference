# Port API AI: Delete Credential Set

Deletes a credential set from Port.

```
DELETE https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/delete-credential-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/delete-credential-set?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/delete-credential-set?${params}`, {
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
| `id` | string | yes | The Port credential set identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `DELETE /apps/:id` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-credential-set.md) for the provider-specific parameters and requirements.

