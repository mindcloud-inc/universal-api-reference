# Loqate: Validate Email

Validates an email address with Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/validate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/validate-email?${params}`, {
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
| `email` | string | yes | The email address to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "duration": 1,
      "emailAddress": "ava@example.com",
      "isComplainerOrFraudRisk": true,
      "isDisposableOrTemporary": true,
      "responseCode": "string",
      "responseMessage": "string",
      "userAccount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `duration` | number |  |
| `emailAddress` | string |  |
| `isComplainerOrFraudRisk` | boolean |  |
| `isDisposableOrTemporary` | boolean |  |
| `responseCode` | string |  |
| `responseMessage` | string |  |
| `userAccount` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /EmailValidation/Interactive/Validate/v2.00/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email.md) for the provider-specific parameters and requirements.

