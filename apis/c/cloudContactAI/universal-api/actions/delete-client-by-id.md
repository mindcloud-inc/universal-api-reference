# CloudContactAI: Delete Client by ID



```
DELETE https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/delete-client-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/delete-client-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/delete-client-by-id?${params}`, {
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
| `id` | string | no | The client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedAt` | date |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `DELETE api/clients/:id` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-client-by-id.md) for the provider-specific parameters and requirements.

