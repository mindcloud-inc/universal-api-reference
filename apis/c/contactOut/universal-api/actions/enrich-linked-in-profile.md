# ContactOut: Enrich LinkedIn Profile

Retrieves profile details from a LinkedIn URL in ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-linked-in-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-linked-in-profile?connectionId=$CONNECTION_ID&profile=https%3A%2F%2Fwww.linkedin.com%2Fin%2Fexample-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profile": "https://www.linkedin.com/in/example-person"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/enrich-linked-in-profile?${params}`, {
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
| `profile` | object | Enriched LinkedIn profile data. |
| `status_code` | number | HTTP-style status code returned by ContactOut. |

## Native endpoint

Through the native ContactOut API, this operation is `GET /v1/linkedin/enrich` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-linked-in-profile.md) for the provider-specific parameters and requirements.

