# Clio Grow: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Grow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | The unique identifier for the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clioId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emails": [
        "ava@example.com"
      ],
      "firstName": "Ava",
      "globalId": "string",
      "id": 1,
      "lastName": "Chen",
      "name": "Ava Chen",
      "phoneNumbers": [
        "string"
      ],
      "status": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clioId` | number |  |
| `createdAt` | date |  |
| `emails` | array<string> |  |
| `firstName` | string |  |
| `globalId` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `name` | string |  |
| `phoneNumbers` | array<string> |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Clio Grow API, this operation is `GET /contacts/{id}` (base URL `https://api.clio.com/grow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

