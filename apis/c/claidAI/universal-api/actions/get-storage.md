# Claid AI: Get Storage

Retrieves a storage connector from Claid AI by storage ID.

```
GET https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/get-storage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Claid AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/get-storage?connectionId=$CONNECTION_ID&storageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/get-storage?${params}`, {
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
| `storageId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "parameters": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Storage identifier. |
| `name` | string | Storage name in Claid. |
| `parameters` | object | Connector-specific storage parameters. |
| `type` | string | Storage connector type. |

## Native endpoint

Through the native Claid AI API, this operation is `GET storage/storages/:storage_id` (base URL `https://api.claid.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-storage.md) for the provider-specific parameters and requirements.

