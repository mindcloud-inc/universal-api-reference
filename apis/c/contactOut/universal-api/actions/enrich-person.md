# ContactOut: Enrich Person

Retrieves a person's profile from ContactOut using multiple identifiers.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-person?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-person?${params}`, {
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
| `company` | string | no | Company name or names. |
| `email` | string | no | Email address of the person. |
| `full_name` | string | no | Full name of the person to enrich. |
| `linkedin_url` | string | no | LinkedIn profile URL of the person. |
| `include` | string | no | Optional contact data to include, such as work_email, personal_email, or phone. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "profile": {
        "company": {
          "domain": "string",
          "name": "Ava Chen"
        },
        "email": "ava@example.com",
        "full_name": "Ava Chen",
        "headline": "string",
        "personal_email": "ava@example.com",
        "phone": "string",
        "url": "https://example.com",
        "work_email": "ava@example.com"
      },
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `profile.company.domain` | string |  |
| `profile.company.name` | string |  |
| `profile.email` | string |  |
| `profile.full_name` | string |  |
| `profile.headline` | string |  |
| `profile.personal_email` | string |  |
| `profile.phone` | string |  |
| `profile.url` | string |  |
| `profile.work_email` | string |  |
| `status_code` | number |  |

## Native endpoint

Through the native ContactOut API, this operation is `POST /v1/people/enrich` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-person.md) for the provider-specific parameters and requirements.

