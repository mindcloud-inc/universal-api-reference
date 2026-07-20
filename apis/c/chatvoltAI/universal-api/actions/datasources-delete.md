# Chatvolt AI: Delete Datasource

Deletes a datasource from Chatvolt AI.

```
DELETE https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datasources-delete
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datasources-delete?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/datasources-delete?${params}`, {
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
| `id` | string | yes | ID of the datasource to be deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "createdAt": "string",
      "groupId": "string",
      "id": "string",
      "lastSynch": "string",
      "name": "Ava Chen",
      "status": "string",
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
| `config` | object | Config. |
| `createdAt` | string | CreatedAt. |
| `groupId` | string | GroupId. |
| `id` | string | Id. |
| `lastSynch` | string | LastSynch. |
| `name` | string | Name. |
| `status` | string | Status. |
| `type` | string | Type. |
| `updatedAt` | string | UpdatedAt. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `DELETE /datasources/{id}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/datasources-delete.md) for the provider-specific parameters and requirements.

