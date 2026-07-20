# IPQS Fraud and Risk Scoring: Search Leaked Email And Password

Retrieves dark web leak matches for an email-password pair from IPQS.

```
GET https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/search-leaked-email-and-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPQS Fraud and Risk Scoring `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/search-leaked-email-and-password?connectionId=$CONNECTION_ID&email=ava%40example.com&password=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "password": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/search-leaked-email-and-password?${params}`, {
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
| `email` | string | yes | Email address to pair with the password for leaked credential search. |
| `password` | string | yes | Plain-text or hashed password to submit in the POST body per IPQS docs. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IPQS Fraud and Risk Scoring API returns.

## Native endpoint

Through the native IPQS Fraud and Risk Scoring API, this operation is `POST /leaked/emailpass/{{credentials.apiKey}}` (base URL `https://www.ipqualityscore.com/api/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-leaked-email-and-password.md) for the provider-specific parameters and requirements.

