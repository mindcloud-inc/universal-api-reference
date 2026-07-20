# Conexteo: Get Model

Retrieves a message template from Conexteo.

```
GET https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/get-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conexteo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/get-model?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conexteo/latest/actions/get-model?${params}`, {
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
| `id` | number | yes | Identifier of the model to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "id": 1,
      "name": "Ava Chen",
      "sender": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Model message content. |
| `id` | number | Model identifier. |
| `name` | string | Model name. |
| `sender` | string | Default sender configured for the model. |

## Native endpoint

Through the native Conexteo API, this operation is `GET /models/:id` (base URL `https://api.conexteo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model.md) for the provider-specific parameters and requirements.

