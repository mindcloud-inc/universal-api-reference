# Greip - Fraud Prevention: Get Email Scoring

Retrieves email risk scoring from Greip.

```
GET https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-email-scoring
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Greip - Fraud Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-email-scoring?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-email-scoring?${params}`, {
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
| `email` | string | yes | The email address to score. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blacklisted": true,
      "domain": {},
      "isDisposable": true,
      "isFree": true,
      "isRoleBased": true,
      "isValid": true,
      "reason": "string",
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blacklisted` | boolean |  |
| `domain` | object |  |
| `isDisposable` | boolean |  |
| `isFree` | boolean |  |
| `isRoleBased` | boolean |  |
| `isValid` | boolean |  |
| `reason` | string |  |
| `score` | number |  |

## Native endpoint

Through the native Greip - Fraud Prevention API, this operation is `GET /scoring/email` (base URL `https://greipapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-scoring.md) for the provider-specific parameters and requirements.

