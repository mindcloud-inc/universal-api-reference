# Cradl AI: Create Function

Creates a new function in Cradl AI.

```
POST https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-function" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-function', {
  method: 'POST',
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
| `name` | string | no | Function name. |
| `description` | string | no | Function description. |
| `runtime` | list | no | Runtime used by the function. One of: `nodejs`, `python`. |
| `metadata` | object | no | Metadata attached to the function. |

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

Through the native Cradl AI API, this operation is `POST /functions` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-function.md) for the provider-specific parameters and requirements.

