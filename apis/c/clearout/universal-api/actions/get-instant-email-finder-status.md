# Clearout: Get Instant Email Finder Status

Retrieves instant email finder queue status from Clearout.

```
GET https://connect.mindcloud.co/v1/universal/clearout/latest/actions/get-instant-email-finder-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clearout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/get-instant-email-finder-status?connectionId=$CONNECTION_ID&qid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "qid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearout/latest/actions/get-instant-email-finder-status?${params}`, {
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
| `qid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "name": "Ava Chen"
      },
      "confidenceScore": 1,
      "domain": "string",
      "emails": {
        "business": "ava@example.com",
        "emailAddress": "ava@example.com",
        "role": "ava@example.com"
      },
      "firstName": "Ava",
      "foundOn": "string",
      "fullName": "Ava Chen",
      "lastName": "Chen",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `company.name` | string |  |
| `confidenceScore` | number |  |
| `domain` | string |  |
| `emails` | array<object> |  |
| `emails.business` | string |  |
| `emails.emailAddress` | string |  |
| `emails.role` | string |  |
| `firstName` | string |  |
| `foundOn` | string |  |
| `fullName` | string |  |
| `lastName` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Clearout API, this operation is `GET /email_finder/instant/queue_status` (base URL `https://api.clearout.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-instant-email-finder-status.md) for the provider-specific parameters and requirements.

