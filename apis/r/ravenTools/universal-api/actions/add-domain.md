# Raven Tools: Add Domain

Creates a new domain in Raven Tools.

```
POST https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/add-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/add-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/add-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | The domain to add to the Raven profile. Default: `codex-raven-tools-default-test.example`. Example: `example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Provider result message. |

## Native endpoint

Through the native Raven Tools API, this operation is `GET /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-domain.md) for the provider-specific parameters and requirements.

