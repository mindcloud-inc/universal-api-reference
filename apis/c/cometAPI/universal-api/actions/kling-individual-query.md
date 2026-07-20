# CometAPI: Kling Individual Query

Retrieves a Kling task from CometAPI.

```
GET https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-individual-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-individual-query?connectionId=$CONNECTION_ID&action=string&action2=string&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "action": "string",
  "action2": "string",
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-individual-query?${params}`, {
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
| `action` | string | yes | Kling resource group. |
| `action2` | string | yes | Kling sub-resource group. |
| `taskId` | string | yes | Kling task identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `status` | string |  |
| `task_id` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `GET /kling/v1/:action/:action2/:task_id` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/kling-individual-query.md) for the provider-specific parameters and requirements.

