# Logit: Get Stack Overview

Retrieves a stack overview from Logit.

```
GET https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-overview?connectionId=$CONNECTION_ID&stackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-overview?${params}`, {
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
      "isDisabled": true,
      "name": "Ava Chen",
      "stackId": "string",
      "stackType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isDisabled` | boolean |  |
| `name` | string |  |
| `stackId` | string |  |
| `stackType` | string |  |

## Native endpoint

Through the native Logit API, this operation is `GET /api/stacks/:stackId` (base URL `https://dashboard.logit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stack-overview.md) for the provider-specific parameters and requirements.

