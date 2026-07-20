# ContactOut: Get Person By Email

Retrieves a LinkedIn profile from an email address in ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-person-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-person-by-email?connectionId=$CONNECTION_ID&email=person%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "person@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-person-by-email?${params}`, {
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
| `email` | string | yes | The email address to look up. Example: `person@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "profile": {
        "email": "ava@example.com",
        "linkedin": "https://example.com"
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
| `profile.linkedin` | string |  |
| `status_code` | number |  |

## Native endpoint

Through the native ContactOut API, this operation is `GET /v1/people/person` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-by-email.md) for the provider-specific parameters and requirements.

