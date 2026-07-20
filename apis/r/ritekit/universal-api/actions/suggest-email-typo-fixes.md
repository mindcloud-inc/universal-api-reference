# Ritekit: Suggest Email Typo Fixes

Retrieves likely typo fixes for an email domain.

```
GET https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/suggest-email-typo-fixes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ritekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/suggest-email-typo-fixes?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/suggest-email-typo-fixes?${params}`, {
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
| `email` | string | yes | Email address to check for likely typos. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "message": "string",
      "result": true,
      "suggestions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `message` | string |  |
| `result` | boolean |  |
| `suggestions` | array<string> |  |

## Native endpoint

Through the native Ritekit API, this operation is `GET /v2/person-insights/email-typo` (base URL `https://api.ritekit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/suggest-email-typo-fixes.md) for the provider-specific parameters and requirements.

