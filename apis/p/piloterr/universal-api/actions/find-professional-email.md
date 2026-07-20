# Piloterr: Find Professional Email



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/find-professional-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/find-professional-email?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/find-professional-email?${params}`, {
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
| `companyDomain` | string | no | Company domain for the email lookup. |
| `companyName` | string | no | Company name for the email lookup. |
| `query` | string | yes | Full name of the person whose professional email you want to find. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidence": 1,
      "email": "ava@example.com",
      "source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidence` | number |  |
| `email` | string |  |
| `source` | string |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /email/finder` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-professional-email.md) for the provider-specific parameters and requirements.

