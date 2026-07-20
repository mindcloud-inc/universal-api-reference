# SendPulse: Update Template

Updates an existing template in SendPulse.

```
PUT https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "345678",
  "body": "PGgxPkhlbGxvIGFnYWluPC9oMT4="
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "345678",
    "body": "PGgxPkhlbGxvIGFnYWluPC9oMT4="
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | The SendPulse template identifier. Example: `345678`. |
| `name` | string | no | Updated name for the template. Example: `Updated Welcome Template`. |
| `body` | string | yes | Updated base64-encoded HTML body for the template. Example: `PGgxPkhlbGxvIGFnYWluPC9oMT4=`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lang` | string | no | Optional template language code. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |

## Native endpoint

Through the native SendPulse API, this operation is `POST /template/edit/:templateId` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

