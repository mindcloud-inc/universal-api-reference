# NeetoInvoice: Get Client

Retrieves details for a client from NeetoInvoice.

```
GET https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoInvoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/get-client?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/get-client?${params}`, {
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
| `clientId` | string | no | Client identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {
        "createdAt": "string",
        "currency": "string",
        "id": "string",
        "name": "Ava Chen",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client.createdAt` | string |  |
| `client.currency` | string |  |
| `client.id` | string |  |
| `client.name` | string |  |
| `client.status` | string |  |

## Native endpoint

Through the native NeetoInvoice API, this operation is `GET /clients/{client_id}` (base URL `https://{{credentials.workspaceSubdomain}}.neetoinvoice.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

