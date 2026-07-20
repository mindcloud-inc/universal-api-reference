# Logit: Get Stack Pipeline Config

Retrieves stack pipeline config from Logit.

```
GET https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-pipeline-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-pipeline-config?connectionId=$CONNECTION_ID&stackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-pipeline-config?${params}`, {
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
| `stackId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configuration": "string",
      "lastUpdated": "string",
      "stale": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | string |  |
| `lastUpdated` | string |  |
| `stale` | boolean |  |

## Native endpoint

Through the native Logit API, this operation is `GET /api/stacks/:stackId/pipeline-config` (base URL `https://dashboard.logit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stack-pipeline-config.md) for the provider-specific parameters and requirements.

