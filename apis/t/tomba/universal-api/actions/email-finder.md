# Tomba: Email Finder

Finds a contact email in Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/email-finder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/email-finder?connectionId=$CONNECTION_ID&domain=string&fullName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "fullName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/email-finder?${params}`, {
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
| `domain` | string | yes | Domain to search for the contact. |
| `fullName` | string | yes | Full name of the contact to look up. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | string | no | Company name to search when a domain is not available. |
| `firstName` | string | no | First name of the contact. |
| `lastName` | string | no | Last name of the contact. |
| `enrichMobile` | boolean | no | Include phone data when available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "country": "string",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "position": "string",
      "score": 1,
      "verification": {
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `country` | string |  |
| `email` | string |  |
| `full_name` | string |  |
| `position` | string |  |
| `score` | number |  |
| `verification.status` | string |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /email-finder` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-finder.md) for the provider-specific parameters and requirements.

