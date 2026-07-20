# Unstructured: Create Destination Connection Check

Creates a destination connection check in Unstructured.

```
POST https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/create-destination-connection-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/create-destination-connection-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/create-destination-connection-check', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destinationId` | string | yes | The destination connector ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "details": {},
      "errorMessage": "string",
      "id": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `details` | object | Additional connection check details. |
| `errorMessage` | string | Connection check error message when verification fails. |
| `id` | string | Connection check ID. |
| `status` | string | Connection check status. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Unstructured API, this operation is `POST /destinations/:destination_id/connection-check` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-destination-connection-check.md) for the provider-specific parameters and requirements.

