# ContactOut: Get Decision Makers With Contact Reveal

Retrieves decision makers with revealed contact information from ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-decision-makers-with-contact-reveal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-decision-makers-with-contact-reveal?connectionId=$CONNECTION_ID&linkedin_url=https%3A%2F%2Flinkedin.com%2Fcompany%2Fcontactout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkedin_url": "https://linkedin.com/company/contactout"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-decision-makers-with-contact-reveal?${params}`, {
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
| `linkedin_url` | string | yes | LinkedIn company URL to inspect for decision makers. Example: `https://linkedin.com/company/contactout`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "metadata": {
        "page": 1,
        "page_size": 1,
        "total_results": 1
      },
      "profiles": "string",
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
| `metadata.page` | number |  |
| `metadata.page_size` | number |  |
| `metadata.total_results` | number |  |
| `profiles` | string |  |
| `status_code` | number |  |

## Native endpoint

Through the native ContactOut API, this operation is `GET /v1/people/decision-makers` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-decision-makers-with-contact-reveal.md) for the provider-specific parameters and requirements.

