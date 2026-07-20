# MailFloss: Get Batch Verification Results

Retrieves batch email verification results from MailFloss.

```
GET https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/get-batch-verification-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailFloss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/get-batch-verification-results?connectionId=$CONNECTION_ID&id=string&next=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "next": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailFloss/latest/actions/get-batch-verification-results?${params}`, {
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
| `id` | string | yes | Batch verification job ID. |
| `next` | number | yes | Next page of results to fetch. |
| `perPage` | number | no | Number of results to return per page. Max 1000; defaults to 100. Default: `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "completedAt": "string",
          "domain": "string",
          "email": "ava@example.com",
          "passed": true,
          "processed": true,
          "reason": "string",
          "status": "string",
          "suggestion": "string"
        }
      ],
      "next": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Batch verification result rows. |
| `data[].completedAt` | string | When verification completed. |
| `data[].domain` | string | Email domain. |
| `data[].email` | string | Verified email address. |
| `data[].passed` | boolean | Whether the email address passed verification. |
| `data[].processed` | boolean | Whether the email address was processed. |
| `data[].reason` | string | Verification category. |
| `data[].status` | string | Verification status. |
| `data[].suggestion` | string | Suggested email address, if available. |
| `next` | string | Next page token or link for additional results. |

## Native endpoint

Through the native MailFloss API, this operation is `GET /batch-verify/:id/results` (base URL `https://api.mailfloss.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-verification-results.md) for the provider-specific parameters and requirements.

