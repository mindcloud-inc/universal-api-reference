# ContactOut: Get LinkedIn Contact Info With Phone

Retrieves contact details and phone for a LinkedIn profile from ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-linked-in-contact-info-with-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-linked-in-contact-info-with-phone?connectionId=$CONNECTION_ID&profile=https%3A%2F%2Fwww.linkedin.com%2Fin%2Fexample-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profile": "https://www.linkedin.com/in/example-person"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-linked-in-contact-info-with-phone?${params}`, {
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
| `profile` | string | yes | The full LinkedIn profile URL. Example: `https://www.linkedin.com/in/example-person`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "profile": {
        "email": "ava@example.com",
        "github": "string",
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
| `profile.email` | string |  |
| `profile.github` | string |  |
| `profile.personal_email` | string |  |
| `profile.phone` | string |  |
| `profile.url` | string |  |
| `profile.work_email` | string |  |
| `status_code` | number |  |

## Native endpoint

Through the native ContactOut API, this operation is `GET /v1/people/linkedin` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-linked-in-contact-info-with-phone.md) for the provider-specific parameters and requirements.

