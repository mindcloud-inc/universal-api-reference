# Infobip: Validate Email Address



```
POST https://connect.mindcloud.co/v1/universal/infobip/latest/actions/validate-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/validate-email-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/validate-email-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | The email address to be validated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "catchAll": true,
      "detailedReasons": "string",
      "didYouMean": "string",
      "disposable": true,
      "reason": "string",
      "risk": "string",
      "roleBased": true,
      "to": "string",
      "validMailbox": "string",
      "validSyntax": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `catchAll` | boolean |  |
| `detailedReasons` | string |  |
| `didYouMean` | string |  |
| `disposable` | boolean |  |
| `reason` | string |  |
| `risk` | string |  |
| `roleBased` | boolean |  |
| `to` | string |  |
| `validMailbox` | string |  |
| `validSyntax` | boolean |  |

## Native endpoint

Through the native Infobip API, this operation is `POST /email/2/validation` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email-address.md) for the provider-specific parameters and requirements.

