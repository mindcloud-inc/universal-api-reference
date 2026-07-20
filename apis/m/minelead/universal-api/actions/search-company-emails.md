# Minelead: Search Company Emails

Finds company emails in Minelead by domain.

```
GET https://connect.mindcloud.co/v1/universal/minelead/latest/actions/search-company-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minelead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minelead/latest/actions/search-company-emails?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minelead/latest/actions/search-company-emails?${params}`, {
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
| `domain` | string | yes | Company domain to search for emails. |
| `name` | string | no | Company name when searching without a domain. |
| `maxEmails` | number | no | Maximum number of emails to display. |
| `generic` | boolean | no | Only return generic emails. |
| `lightMode` | boolean | no | Only display already found emails. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "emails": [
        {}
      ],
      "extensive": true,
      "name": "Ava Chen",
      "pattern": "string",
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
| `domain` | string |  |
| `emails` | array<object> |  |
| `extensive` | boolean |  |
| `name` | string |  |
| `pattern` | string |  |
| `status` | string |  |
| `timestamp` | number |  |

## Native endpoint

Through the native Minelead API, this operation is `GET /search` (base URL `https://api.minelead.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-company-emails.md) for the provider-specific parameters and requirements.

