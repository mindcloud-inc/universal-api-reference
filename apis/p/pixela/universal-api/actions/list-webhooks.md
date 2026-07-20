# Pixela: List Webhooks

Retrieves all webhook definitions from Pixela.

```
GET https://connect.mindcloud.co/v1/universal/pixela/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pixela `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixela/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixela/latest/actions/list-webhooks?${params}`, {
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
| `username` | string | yes | Pixela username in the request path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "graphID": "string",
      "quantity": "string",
      "type": "string",
      "webhookHash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `graphID` | string |  |
| `quantity` | string |  |
| `type` | string |  |
| `webhookHash` | string |  |

## Native endpoint

Through the native Pixela API, this operation is `GET /v1/users/:username/webhooks` (base URL `https://pixe.la`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

