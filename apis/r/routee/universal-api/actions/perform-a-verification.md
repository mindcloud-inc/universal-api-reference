# Routee: Perform a verification

Creates a new verification in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-a-verification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-a-verification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "method": "string",
  "type": "string",
  "recipient": "string",
  "template": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/perform-a-verification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "method": "string",
    "type": "string",
    "recipient": "string",
    "template": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `method` | string | yes | The method which will be used to send the 2step verification. Values: "sms", "voice". |
| `type` | string | yes | The type of the message. Value: "code". |
| `recipient` | string | yes | The recipient that will receive the 2step verification. For sms method format with a '+' and country code e.g., +306948530920 (E.164 format). |
| `template` | string | yes | The template of the message. It must contain a @@pin that will be replaced by the generated code. |
| `arguments` | string | no | If the template is for example '@@name your code is @@pin' and the argument has a property name: 'Nick' the message will be 'Nick your code is 4232'. Note that if the template contains a @@ placeholder and a value is not present in the arguments property it will stay as is. |
| `templateCountry` | string | no | Country in [ISO-3166-1](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2#Officially_assigned_code_elements) alpha 2 format (GR, US etc.). The country to use in order to select a translated template (if defined in Routee web interface) |
| `originator` | string | no | The senderId that will be set when sending the SMS |
| `lifetimeInSeconds` | number | no | How many seconds this verification will remain active. After that time passes the verification status will be Expired. |
| `maxRetries` | number | no | Defines the number of times the user can re-confirm the verification before the verification changes its state to Failed. |
| `digits` | number | no | The number of digits of the generated random numeric code. |
| `restrictions` | object | no | [OPTIONAL] Provide the registered Content Template ID and Principal Entity ID to ensure the message is not rejected by TRAI regulations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresAt": "string",
      "maxRetries": 1,
      "status": "string",
      "timesTried": 1,
      "trackingId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | string |  |
| `maxRetries` | number |  |
| `status` | string |  |
| `timesTried` | number |  |
| `trackingId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /2step` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/perform-a-verification.md) for the provider-specific parameters and requirements.

