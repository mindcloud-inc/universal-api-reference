# Hunter: Count Domain Emails



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/count-domain-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/count-domain-emails?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/count-domain-emails?${params}`, {
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
| `domain` | string | yes | Company domain to count emails for. |
| `company` | string | no |  |
| `type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "department": {},
      "genericEmails": 1,
      "personalEmails": 1,
      "seniority": {},
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `department` | object |  |
| `genericEmails` | number |  |
| `personalEmails` | number |  |
| `seniority` | object |  |
| `total` | number |  |

## Native endpoint

Through the native Hunter API, this operation is `GET /email-count` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-domain-emails.md) for the provider-specific parameters and requirements.

