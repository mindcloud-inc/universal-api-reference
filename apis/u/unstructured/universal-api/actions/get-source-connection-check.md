# Unstructured: Get Source Connection Check

Retrieves a source connection check from Unstructured.

```
GET https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-source-connection-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-source-connection-check?connectionId=$CONNECTION_ID&sourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-source-connection-check?${params}`, {
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
| `sourceId` | string | yes | The source connector ID. |

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

Through the native Unstructured API, this operation is `GET /sources/:source_id/connection-check` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-source-connection-check.md) for the provider-specific parameters and requirements.

