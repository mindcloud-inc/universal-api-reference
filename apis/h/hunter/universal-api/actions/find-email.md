# Hunter: Find Email



```
GET https://connect.mindcloud.co/v1/universal/hunter/latest/actions/find-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hunter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hunter/latest/actions/find-email?connectionId=$CONNECTION_ID&domain=string&firstName=Ava&lastName=Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "firstName": "Ava",
  "lastName": "Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hunter/latest/actions/find-email?${params}`, {
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
| `domain` | string | yes | Company domain, like hunter.io. |
| `firstName` | string | yes | Person's first name. |
| `lastName` | string | yes | Person's last name. |
| `company` | string | no | Company name when a domain is not provided. |
| `linkedinHandle` | string | no |  |
| `fullName` | string | no |  |
| `maxDuration` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptAll": true,
      "company": "string",
      "domain": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "linkedinUrl": "https://example.com",
      "phoneNumber": "string",
      "position": "string",
      "score": 1,
      "sources": [
        {}
      ],
      "twitter": "string",
      "verification": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptAll` | boolean |  |
| `company` | string |  |
| `domain` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `linkedinUrl` | string |  |
| `phoneNumber` | string |  |
| `position` | string |  |
| `score` | number |  |
| `sources` | array<object> |  |
| `twitter` | string |  |
| `verification` | object |  |

## Native endpoint

Through the native Hunter API, this operation is `GET /email-finder` (base URL `https://api.hunter.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-email.md) for the provider-specific parameters and requirements.

