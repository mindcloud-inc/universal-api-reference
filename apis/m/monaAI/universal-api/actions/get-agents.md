# Mona AI: Get Agents

Retrieves agents from Mona AI.

```
GET https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mona AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monaAI/latest/actions/get-agents?${params}`, {
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
| `category` | string | no | Filter agents by category. |
| `isActive` | boolean | no | Filter agents by active state. |
| `typeOfAgent` | string | no | Filter agents by type, such as multi. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": {
        "multi": 1,
        "single": 1,
        "total": 1,
        "workflow": 1
      },
      "data": [
        {}
      ],
      "grouped": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | object | Agent counts by type. |
| `count.multi` | number | Number of multi agents. |
| `count.single` | number | Number of single agents. |
| `count.total` | number | Total number of agents. |
| `count.workflow` | number | Number of workflow agents. |
| `data` | array<object> | Agent records returned by Mona. |
| `grouped` | object | Agents grouped by Mona agent type. |

## Native endpoint

Through the native Mona AI API, this operation is `POST /database/getAgentsFromDatabase` (base URL `https://api.mona-ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agents.md) for the provider-specific parameters and requirements.

