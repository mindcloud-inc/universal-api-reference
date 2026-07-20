# xMatters: Modify a form message template

Updates a form message template in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-form-message-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-form-message-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-a-form-message-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": [
        {
          "body": "ava@example.com",
          "language": "ava@example.com",
          "subject": "ava@example.com"
        }
      ],
      "language": "string",
      "sms": [
        {
          "language": "string",
          "text": "string"
        }
      ],
      "voice": [
        {
          "steps": [
            {
              "commonProperty": "string",
              "formProperty": {
                "name": "Ava Chen"
              },
              "id": "string",
              "phrase": "string",
              "playback": "string",
              "stepType": "string"
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email[].body` | string |  |
| `email[].language` | string |  |
| `email[].subject` | string |  |
| `language` | string |  |
| `sms[].language` | string |  |
| `sms[].text` | string |  |
| `voice[].steps[].commonProperty` | string |  |
| `voice[].steps[].formProperty.name` | string |  |
| `voice[].steps[].id` | string |  |
| `voice[].steps[].phrase` | string |  |
| `voice[].steps[].playback` | string |  |
| `voice[].steps[].stepType` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST forms/{formId}/message-templates` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-a-form-message-template.md) for the provider-specific parameters and requirements.

