# Bika.ai: List Automation Triggers



```
GET https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-automation-triggers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bika.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-automation-triggers?connectionId=$CONNECTION_ID&nodeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "nodeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/list-automation-triggers?${params}`, {
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
| `nodeId` | string | yes | Automation node ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "status": "string",
          "type": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | array<object> |  |
| `data[].createdAt` | date |  |
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].status` | string |  |
| `data[].type` | string |  |
| `data[].updatedAt` | date |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Bika.ai API, this operation is `GET /automations/:nodeId/triggers` (base URL `https://bika.ai/api/openapi/bika/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-automation-triggers.md) for the provider-specific parameters and requirements.

