# zipBoard: Remove Project Collaborator

Removes a project collaborator from zipBoard.

```
DELETE https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/remove-project-collaborator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/remove-project-collaborator?connectionId=$CONNECTION_ID&email=ava%40example.com&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/remove-project-collaborator?${params}`, {
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
| `email` | string | yes |  |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Collaborator email address. |
| `id` | string | Collaborator identifier. |
| `name` | string | Collaborator name. |

## Native endpoint

Through the native zipBoard API, this operation is `DELETE /project/:id/collaborators` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-project-collaborator.md) for the provider-specific parameters and requirements.

