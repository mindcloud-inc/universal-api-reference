# Infobip: Request Email Validations



```
POST https://connect.mindcloud.co/v1/universal/infobip/latest/actions/request-email-validations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/request-email-validations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinations": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/request-email-validations', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinations": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `validationRequestId` | string | no | Unique identifier for the bulk email validation request. Provide your own or leave it blank to have one generated automatically. |
| `destinations` | list<object> | yes | Array of email addresses to be validated. |
| `destinations.destination` | string | no | The email address to be validated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "validationRequestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `validationRequestId` | string |  |

## Native endpoint

Through the native Infobip API, this operation is `POST /email/2/validations` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-email-validations.md) for the provider-specific parameters and requirements.

