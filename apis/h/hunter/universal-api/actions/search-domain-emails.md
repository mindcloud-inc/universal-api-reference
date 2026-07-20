# Hunter: Search Domain Emails



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/search-domain-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/search-domain-emails?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/search-domain-emails?${params}`, {
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
| `domain` | string | yes | Domain name to search, like hunter.io. |
| `company` | string | no | Company name to search when a domain is not provided. |
| `limit` | number | no | Maximum number of email addresses to return. |
| `offset` | number | no | Number of results to skip. |
| `type` | string | no | Filter to personal or generic email addresses. |
| `seniority` | string | no | Comma-delimited seniority filters. |
| `department` | string | no | Comma-delimited department filters. |
| `requiredField` | string | no | Comma-delimited fields that must be present. |
| `verificationStatus` | string | no | Comma-delimited verification status filters. |
| `jobTitles` | string | no | Comma-delimited job title filters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptAll": true,
      "disposable": true,
      "domain": "string",
      "emails": [
        {}
      ],
      "linkedDomains": [
        "https://example.com"
      ],
      "organization": "string",
      "pattern": "string",
      "webmail": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptAll` | boolean |  |
| `disposable` | boolean |  |
| `domain` | string |  |
| `emails` | array<object> |  |
| `linkedDomains` | array<string> |  |
| `organization` | string |  |
| `pattern` | string |  |
| `webmail` | boolean |  |

## Native endpoint

Through the native Hunter API, this operation is `GET /domain-search` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-domain-emails.md) for the provider-specific parameters and requirements.

