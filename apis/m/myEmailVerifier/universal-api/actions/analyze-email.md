# MyEmailVerifier: Analyze Email

Analyzes an email address in MyEmailVerifier.

```
GET https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/analyze-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyEmailVerifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/analyze-email?connectionId=$CONNECTION_ID&email=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myEmailVerifier/latest/actions/analyze-email?${params}`, {
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
| `email` | string | yes | The email address to analyze. Example: `name@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysis": {},
      "api_info": {},
      "email": "ava@example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysis` | object | Structured email-analysis result from MyEmailVerifier. |
| `api_info` | object | Credit and version metadata for the analysis request. |
| `email` | string | Email address that was analyzed. |
| `status` | string | Whether the analysis call succeeded. |

## Native endpoint

Through the native MyEmailVerifier API, this operation is `GET /email-analysis/analyze/:email/{{credentials.apiKey}}` (base URL `https://client.myemailverifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-email.md) for the provider-specific parameters and requirements.

