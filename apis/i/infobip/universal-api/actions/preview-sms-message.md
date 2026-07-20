# Infobip: Preview SMS Message



```
GET https://connect.mindcloud.co/v1/universal/infobip/latest/actions/preview-sms-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/preview-sms-message?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infobip/latest/actions/preview-sms-message?${params}`, {
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
| `text` | string | yes | Content of the message being sent. |
| `languageCode` | string | no | [Language code](https://www.infobip.com/docs/sms/language#national-language-identifier) for the correct character set. `AUTODETECT` lets the platform select the character set based on message content only for supported languages. |
| `transliteration` | string | no | The transliteration of your sent message from one script to another. [Transliteration](https://www.infobip.com/docs/sms/language#sms-transliteration) is used to replace characters which are not recognized as part of your defaulted alphabet. `ALL` means that the transliteration process will recognize all supported languages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "originalText": "string",
      "previews": {
        "charactersRemaining": 1,
        "configuration": {
          "language": {},
          "transliteration": "string"
        },
        "messageCount": 1,
        "textPreview": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `originalText` | string |  |
| `previews` | array<object> |  |
| `previews.charactersRemaining` | number |  |
| `previews.configuration` | object |  |
| `previews.configuration.language` | object |  |
| `previews.configuration.transliteration` | string |  |
| `previews.messageCount` | number |  |
| `previews.textPreview` | string |  |

## Native endpoint

Through the native Infobip API, this operation is `POST /sms/1/preview` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-sms-message.md) for the provider-specific parameters and requirements.

