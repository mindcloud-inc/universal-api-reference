# LEADTEX: Send File By External ID

Sends a file message in LEADTEX by external contact ID.

```
POST https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/send-file-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LEADTEX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/send-file-by-external-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bot_id": 1,
  "contact_external_id": "string",
  "file": "string",
  "messenger": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lEADTEX/latest/actions/send-file-by-external-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bot_id": 1,
    "contact_external_id": "string",
    "file": "string",
    "messenger": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bot_id` | number | yes | ID of the bot associated with the contact. |
| `contact_external_id` | string | yes | Phone number or external messenger/social ID for the contact. |
| `file` | string | yes | URL of the file to send. |
| `messenger` | string | yes | Messenger identifier such as whatsapp, telegram, viber, or icq. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "errors": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `errors` | object |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native LEADTEX API, this operation is `POST /sendMessage?api_token={{credentials.apiKey}}` (base URL `https://app.leadteh.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-file-by-external-id.md) for the provider-specific parameters and requirements.

