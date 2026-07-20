# Lettr: Create Domain



```
POST https://connect.mindcloud.co/v1/universal/lettr/latest/actions/create-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/create-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lettr/latest/actions/create-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | Sending domain to register. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "dkim": {
          "headers": "string",
          "public": "string",
          "selector": "string",
          "signing_domain": "string"
        },
        "domain": "string",
        "status": "string",
        "status_label": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Created domain payload. |
| `data.dkim` | object | DKIM setup details. |
| `data.dkim.headers` | string | Signed header list. |
| `data.dkim.public` | string | DKIM public key. |
| `data.dkim.selector` | string | DKIM selector. |
| `data.dkim.signing_domain` | string | Signing domain. |
| `data.domain` | string | Sending domain name. |
| `data.status` | string | Domain status code. |
| `data.status_label` | string | Human-readable domain status. |
| `message` | string | Domain creation status message. |

## Native endpoint

Through the native Lettr API, this operation is `POST /domains` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-domain.md) for the provider-specific parameters and requirements.

