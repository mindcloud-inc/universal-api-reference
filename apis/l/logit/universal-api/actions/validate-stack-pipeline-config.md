# Logit: Validate Stack Pipeline Config

Validates stack pipeline config in Logit.

```
GET https://connect.mindcloud.co/v1/universal/logit/latest/actions/validate-stack-pipeline-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logit/latest/actions/validate-stack-pipeline-config?connectionId=$CONNECTION_ID&stackId=string&testConfiguration=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string",
  "testConfiguration": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logit/latest/actions/validate-stack-pipeline-config?${params}`, {
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
| `testConfiguration` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Logit API, this operation is `POST /api/stacks/:stackId/pipeline-config/validation` (base URL `https://dashboard.logit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-stack-pipeline-config.md) for the provider-specific parameters and requirements.

