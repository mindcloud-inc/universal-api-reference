# ContactOut: Batch Get LinkedIn Contact Info

Retrieves contact details for LinkedIn profiles in bulk from ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/batch-get-linked-in-contact-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/batch-get-linked-in-contact-info?connectionId=$CONNECTION_ID&profiles=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profiles": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/batch-get-linked-in-contact-info?${params}`, {
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
| `profiles` | string | yes | An array of LinkedIn profile URLs. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
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
| `profiles` | object | Map of LinkedIn profile URLs to the contact emails returned for each profile. |
| `status_code` | number | HTTP-style status code returned by ContactOut. |

## Native endpoint

Through the native ContactOut API, this operation is `POST /v1/people/linkedin/batch` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-get-linked-in-contact-info.md) for the provider-specific parameters and requirements.

