# Routee: Analyse an SMS message

Analyzes an SMS message in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/analyse-an-sms-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/analyse-an-sms-message?connectionId=$CONNECTION_ID&from=string&body=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string",
  "body": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/analyse-an-sms-message?${params}`, {
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
| `from` | string | yes | The sender of the message. This can be a telephone number (numeric string with maximum length 16 characters) or an alphanumeric string (maximum length 11 characters). When you want to use a [number](/docs/numbers), you have to enter it without the '+' before the country code (eg 447123123456). |
| `body` | string | yes | The message you want to send. |
| `to` | string | yes | The destination phone number. Format with a '+' and country code e.g., +306948530920 (E.164 format). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bodyAnalysis": {
        "characters": 1,
        "parts": 1,
        "unicode": true
      },
      "cost": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bodyAnalysis` | object |  |
| `bodyAnalysis.characters` | number |  |
| `bodyAnalysis.parts` | number |  |
| `bodyAnalysis.unicode` | boolean |  |
| `cost` | number |  |

## Native endpoint

Through the native Routee API, this operation is `POST /sms/analyze` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyse-an-sms-message.md) for the provider-specific parameters and requirements.

