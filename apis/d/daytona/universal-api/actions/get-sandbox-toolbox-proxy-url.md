# Daytona: Get Sandbox Toolbox Proxy URL

Retrieves the sandbox toolbox proxy URL from Daytona.

```
GET https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-sandbox-toolbox-proxy-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-sandbox-toolbox-proxy-url?connectionId=$CONNECTION_ID&sandboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sandboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-sandbox-toolbox-proxy-url?${params}`, {
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
| `sandboxId` | string | yes | ID of the sandbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | The toolbox proxy URL for the sandbox. |

## Native endpoint

Through the native Daytona API, this operation is `GET /sandbox/[:sandboxId]/toolbox-proxy-url` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sandbox-toolbox-proxy-url.md) for the provider-specific parameters and requirements.

