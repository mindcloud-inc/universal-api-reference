# Unstructured: Get Destination Connector

Retrieves a destination connector from Unstructured.

```
GET https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-destination-connector
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-destination-connector?connectionId=$CONNECTION_ID&destinationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "destinationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-destination-connector?${params}`, {
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
| `destinationId` | string | yes | The destination connector ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Unstructured API, this operation is `GET /destinations/:destination_id` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-destination-connector.md) for the provider-specific parameters and requirements.

