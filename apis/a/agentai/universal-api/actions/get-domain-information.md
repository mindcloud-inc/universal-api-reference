# Agent.ai: Get Domain Information

Retrieves domain registration data from Agent.ai by domain.

```
GET https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-domain-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-domain-information?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-domain-information?${params}`, {
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
| `domain` | string | yes | Domain name to retrieve information for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object |  |
| `status` | number |  |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/domain_info` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-information.md) for the provider-specific parameters and requirements.

