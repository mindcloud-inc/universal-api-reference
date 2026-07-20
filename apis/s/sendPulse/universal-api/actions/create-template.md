# SendPulse: Create Template

Creates a new template in SendPulse.

```
POST https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Welcome Template",
  "body": "PGgxPkhlbGxvPC9oMT4="
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Welcome Template",
    "body": "PGgxPkhlbGxvPC9oMT4="
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the template. Example: `Welcome Template`. |
| `body` | string | yes | Base64-encoded HTML body for the template. Example: `PGgxPkhlbGxvPC9oMT4=`. |

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
      "real_id": 1,
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `real_id` | number |  |
| `result` | boolean |  |

## Native endpoint

Through the native SendPulse API, this operation is `POST /template` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

