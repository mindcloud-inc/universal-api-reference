# Cradl AI: Get Function

Retrieves a function from Cradl AI.

```
GET https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/get-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/get-function?connectionId=$CONNECTION_ID&functionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "functionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/get-function?${params}`, {
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
| `functionId` | string | yes | Identifier of the function. |

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

Through the native Cradl AI API, this operation is `GET /functions/:functionId` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-function.md) for the provider-specific parameters and requirements.

