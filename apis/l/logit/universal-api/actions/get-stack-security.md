# Logit: Get Stack Security

Retrieves stack security details from Logit.

```
GET https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-security
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-security?connectionId=$CONNECTION_ID&stackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-security?${params}`, {
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
| `stackId` | string | yes | The ID of a Logit stack. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firewallRules": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firewallRules` | array<object> |  |

## Native endpoint

Through the native Logit API, this operation is `GET /api/stacks/:stackId/security` (base URL `https://dashboard.logit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stack-security.md) for the provider-specific parameters and requirements.

