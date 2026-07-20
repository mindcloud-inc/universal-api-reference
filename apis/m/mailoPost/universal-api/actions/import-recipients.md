# MailoPost: Import Recipients

Imports recipients into a MailoPost list.

```
POST https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/import-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/import-recipients" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "recipients[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/import-recipients', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "recipients[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | MailoPost recipient list identifier. |
| `recipients[]` | array<object> | yes | Recipients to import. |
| `tags[]` | array<string> | no | Tags applied to imported recipients. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `runTriggers` | string | no | Run triggers during import. Example: `trigger_fresh`. |
| `callbackUrl` | string | no | Callback URL called when import completes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callback_url": "https://example.com",
      "id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callback_url` | string |  |
| `id` | number |  |
| `status` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `POST /email/lists/:id/recipients/imports` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-recipients.md) for the provider-specific parameters and requirements.

