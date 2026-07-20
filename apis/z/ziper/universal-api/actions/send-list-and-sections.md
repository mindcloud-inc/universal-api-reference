# Ziper: Send List And Sections

Sends a WhatsApp list message with sections using Ziper.

```
POST https://connect.mindcloud.co/v1/universal/ziper/latest/actions/send-list-and-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ziper/latest/actions/send-list-and-sections" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "string",
  "text": "string",
  "title": "string",
  "buttonText": "string",
  "sections[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ziper/latest/actions/send-list-and-sections', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "string",
    "text": "string",
    "title": "string",
    "buttonText": "string",
    "sections[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `number` | string | yes | WhatsApp phone number in country-code plus phone-number format. |
| `text` | string | yes | Main list message text. |
| `footer` | string | no | Optional footer text for the list message. |
| `title` | string | yes | Bold list title. |
| `buttonText` | string | yes | Text on the button that opens the list. |
| `sections[]` | array<object> | yes | List sections array as documented by Ziper. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider result message. |
| `status` | string | Provider status returned by Ziper. |

## Native endpoint

Through the native Ziper API, this operation is `POST /send.php` (base URL `https://ziper.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-list-and-sections.md) for the provider-specific parameters and requirements.

