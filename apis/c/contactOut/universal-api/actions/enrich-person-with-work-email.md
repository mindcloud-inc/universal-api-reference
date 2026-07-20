# ContactOut: Enrich Person With Work Email

Retrieves a person's profile and work email from ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-person-with-work-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-person-with-work-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-person-with-work-email?${params}`, {
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
| `full_name` | string | no | Full name of the person to enrich. |
| `linkedin_url` | string | no | LinkedIn profile URL of the person. |

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
| `profile` | object | Enriched person profile with work email coverage. |
| `status_code` | number | HTTP-style status code returned by ContactOut. |

## Native endpoint

Through the native ContactOut API, this operation is `POST /v1/people/enrich` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-person-with-work-email.md) for the provider-specific parameters and requirements.

