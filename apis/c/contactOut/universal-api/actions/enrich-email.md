# ContactOut: Enrich Email

Retrieves profile details from an email address in ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-email?connectionId=$CONNECTION_ID&email=person%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "person@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-email?${params}`, {
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
| `email` | string | yes | The email address to enrich. Example: `person@example.com`. |
| `include` | string | no | Optional extra data to return. ContactOut currently supports work_email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "profile": {},
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | API response message. |
| `profile` | object | Enriched person profile returned for the email address. |
| `status_code` | number | HTTP-style status code returned by ContactOut. |

## Native endpoint

Through the native ContactOut API, this operation is `GET /v1/email/enrich` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-email.md) for the provider-specific parameters and requirements.

