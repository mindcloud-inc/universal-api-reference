# Unstructured: Delete Source Connector

Deletes a source connector from Unstructured.

```
DELETE https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/delete-source-connector
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/delete-source-connector?connectionId=$CONNECTION_ID&sourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/delete-source-connector?${params}`, {
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

Through the native Unstructured API, this operation is `DELETE /sources/:source_id` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-source-connector.md) for the provider-specific parameters and requirements.

