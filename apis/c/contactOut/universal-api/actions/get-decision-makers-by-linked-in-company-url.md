# ContactOut: Get Decision Makers By LinkedIn Company URL

Retrieves decision makers by LinkedIn company URL from ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-decision-makers-by-linked-in-company-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-decision-makers-by-linked-in-company-url?connectionId=$CONNECTION_ID&linkedin_url=https%3A%2F%2Flinkedin.com%2Fcompany%2Fcontactout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkedin_url": "https://linkedin.com/company/contactout"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-decision-makers-by-linked-in-company-url?${params}`, {
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
| `profiles` | object | Map of LinkedIn profile URLs to decision-maker profile summaries. |
| `status_code` | number | HTTP-style status code returned by ContactOut. |

## Native endpoint

Through the native ContactOut API, this operation is `GET /v1/people/decision-makers` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-decision-makers-by-linked-in-company-url.md) for the provider-specific parameters and requirements.

