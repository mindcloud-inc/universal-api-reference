# Minelead: Detect Disposable Email

Checks whether an email address is disposable in Minelead.

```
GET https://connect.mindcloud.co/v1/universal/minelead/latest/actions/detect-disposable-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minelead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minelead/latest/actions/detect-disposable-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minelead/latest/actions/detect-disposable-email?${params}`, {
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
| `email` | string | yes | Email address to inspect for disposability. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "a_record_status": "string",
      "disposability_score": "string",
      "disposable_status": "string",
      "domain_type": "string",
      "email": "ava@example.com",
      "format_valid": true,
      "mx_record_status": "string",
      "ptr_record_status": "string",
      "spam_score": "string",
      "status": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `a_record_status` | string |  |
| `disposability_score` | string |  |
| `disposable_status` | string |  |
| `domain_type` | string |  |
| `email` | string |  |
| `format_valid` | boolean |  |
| `mx_record_status` | string |  |
| `ptr_record_status` | string |  |
| `spam_score` | string |  |
| `status` | string |  |
| `timestamp` | number |  |

## Native endpoint

Through the native Minelead API, this operation is `GET /detect-disposable` (base URL `https://api.minelead.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-disposable-email.md) for the provider-specific parameters and requirements.

