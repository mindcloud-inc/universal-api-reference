# NeetoInvoice: Update Client Status

Updates a client status in NeetoInvoice.

```
PUT https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/update-client-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoInvoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/update-client-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neetoInvoice/latest/actions/update-client-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | no | Client identifier whose status will be updated. |
| `status` | string | no | New client status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {
        "id": "string",
        "status": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client.id` | string |  |
| `client.status` | string |  |
| `message` | string |  |

## Native endpoint

Through the native NeetoInvoice API, this operation is `POST /clients/update_status` (base URL `https://{{credentials.workspaceSubdomain}}.neetoinvoice.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client-status.md) for the provider-specific parameters and requirements.

