# Stack AI: Get Action Options



```
GET https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-action-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-action-options?connectionId=$CONNECTION_ID&configName=Ava%20Chen&providerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "configName": "Ava Chen",
  "providerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/get-action-options?${params}`, {
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
| `configName` | string | yes | The config field whose options should be fetched. |
| `providerId` | string | yes | The provider identifier. |
| `actionId` | string | no | The action identifier. |
| `triggerId` | string | no | The trigger identifier. |
| `connectionId` | string | no | The connection identifier. |
| `parameters` | object | no | Additional parameter values used to resolve dependent options. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Stack AI API, this operation is `POST /tools/options` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action-options.md) for the provider-specific parameters and requirements.

