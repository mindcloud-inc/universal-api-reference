# Tailwind: List Boards

Retrieves boards from Tailwind.

```
GET https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/list-boards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tailwind `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/list-boards?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tailwind/latest/actions/list-boards?${params}`, {
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
| `accountId` | string | yes | Pinterest account ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isCollaborator": true,
      "isSecret": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Board ID. |
| `isCollaborator` | boolean | Whether the user is a collaborator. |
| `isSecret` | boolean | Whether the board is secret. |
| `name` | string | Board name. |

## Native endpoint

Through the native Tailwind API, this operation is `GET /v1/accounts/:accountId/boards` (base URL `https://api-v1.tailwind.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-boards.md) for the provider-specific parameters and requirements.

