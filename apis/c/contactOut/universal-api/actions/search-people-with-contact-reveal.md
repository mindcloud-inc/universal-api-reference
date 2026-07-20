# ContactOut: Search People With Contact Reveal

Finds people in ContactOut with revealed contact information.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-people-with-contact-reveal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-people-with-contact-reveal?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-people-with-contact-reveal?${params}`, {
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
| `company` | string | no | Filter by current or past company. |
| `job_title` | string | no | Filter by job title. |
| `name` | string | no | Match people by name. |
| `page` | string | no | Results page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "metadata": {},
      "profiles": {},
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
| `metadata` | object | Paging and result metadata. |
| `profiles` | object | Map of LinkedIn profile URLs to people search results with revealed contact data. |
| `status_code` | number | HTTP-style status code returned by ContactOut. |

## Native endpoint

Through the native ContactOut API, this operation is `POST /v1/people/search` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-people-with-contact-reveal.md) for the provider-specific parameters and requirements.

