# Email Hippo: Verify Email (MORE V3 JSON)

Verifies an email address with Email Hippo MORE V3 JSON.

```
GET https://connect.mindcloud.co/v1/universal/emailHippo/latest/actions/verify-email-morev3-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Email Hippo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailHippo/latest/actions/verify-email-morev3-json?connectionId=$CONNECTION_ID&emailAddress=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailAddress": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailHippo/latest/actions/verify-email-morev3-json?${params}`, {
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
| `emailAddress` | string | yes | The email address to verify. Example: `name@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "diagnostic": {},
      "disposition": {},
      "domain": "string",
      "emailVerification": {},
      "hippoTrust": {},
      "infrastructure": {},
      "meta": {},
      "performance": {},
      "sendAssess": {},
      "social": {},
      "spamAssess": {},
      "spamTrapAssess": {},
      "version": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `diagnostic` | object |  |
| `disposition` | object |  |
| `domain` | string |  |
| `emailVerification` | object |  |
| `hippoTrust` | object |  |
| `infrastructure` | object |  |
| `meta` | object |  |
| `performance` | object |  |
| `sendAssess` | object |  |
| `social` | object |  |
| `spamAssess` | object |  |
| `spamTrapAssess` | object |  |
| `version` | object |  |

## Native endpoint

Through the native Email Hippo API, this operation is `GET v3/more/json/{{credentials.apiKey}}/:emailAddress` (base URL `https://api.hippoapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-morev3-json.md) for the provider-specific parameters and requirements.

