# ZeroBounce: Find Email

Finds contact emails in ZeroBounce by domain or company.

```
GET https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/find-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZeroBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/find-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeroBounce/latest/actions/find-email?${params}`, {
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
| `domain` | string | no |  |
| `companyName` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `middleName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "didYouMean": "string",
      "domain": "string",
      "email": "ava@example.com",
      "emailConfidence": "ava@example.com",
      "failureReason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string | Company name returned by ZeroBounce when available. |
| `didYouMean` | string | Suggested correction when the request likely contains a typo. |
| `domain` | string | The domain used for the lookup. |
| `email` | string | The inferred email address. |
| `emailConfidence` | string | ZeroBounce confidence level for the inferred email. |
| `failureReason` | string | Reason returned when no email pattern can be inferred. |

## Native endpoint

Through the native ZeroBounce API, this operation is `GET /v2/guessformat` (base URL `https://api.zerobounce.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-email.md) for the provider-specific parameters and requirements.

