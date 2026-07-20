# Cradl AI: Update Function

Updates an existing function in Cradl AI.

```
PUT https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/update-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/update-function" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "functionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/update-function', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "functionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `functionId` | string | yes | Identifier of the function to update. |
| `name` | string | no | Updated function name. |
| `description` | string | no | Updated function description. |
| `metadata` | object | no | Updated metadata attached to the function. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "fileUrl": "https://example.com",
      "functionId": "string",
      "id": "string",
      "managedCodeId": "string",
      "metadata": {},
      "name": "Ava Chen",
      "organizationId": "string",
      "runtime": "string",
      "updatedBy": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string |  |
| `createdTime` | date |  |
| `description` | string |  |
| `fileUrl` | string |  |
| `functionId` | string |  |
| `id` | string |  |
| `managedCodeId` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `organizationId` | string |  |
| `runtime` | string |  |
| `updatedBy` | string |  |
| `updatedTime` | date |  |

## Native endpoint

Through the native Cradl AI API, this operation is `PATCH /functions/:functionId` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-function.md) for the provider-specific parameters and requirements.

