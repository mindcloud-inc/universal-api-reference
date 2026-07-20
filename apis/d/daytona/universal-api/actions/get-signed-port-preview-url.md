# Daytona: Get Signed Port Preview URL

Retrieves a signed sandbox port preview URL from Daytona.

```
GET https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-signed-port-preview-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-signed-port-preview-url?connectionId=$CONNECTION_ID&sandboxIdOrName=Ava%20Chen&port=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sandboxIdOrName": "Ava Chen",
  "port": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-signed-port-preview-url?${params}`, {
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
| `sandboxIdOrName` | string | yes | ID or name of the sandbox. |
| `port` | number | yes | Port number to get signed preview URL for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "port": 1,
      "sandboxId": "string",
      "token": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `port` | number | Port number of the signed preview URL. |
| `sandboxId` | string | ID of the sandbox. |
| `token` | string | Token of the signed preview URL. |
| `url` | string | Signed preview URL. |

## Native endpoint

Through the native Daytona API, this operation is `GET /sandbox/[:sandboxIdOrName]/ports/[:port]/signed-preview-url` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signed-port-preview-url.md) for the provider-specific parameters and requirements.

