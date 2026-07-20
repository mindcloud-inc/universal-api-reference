# Sequenzy: Get Recipient Metrics by Email

Retrieves recipient engagement metrics from Sequenzy by email.

```
GET https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-recipient-metrics-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sequenzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-recipient-metrics-by-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-recipient-metrics-by-email?${params}`, {
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
| `email` | string | no | Filter to a single recipient by email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "limit": 1,
        "page": 1,
        "total": 1,
        "totalPages": 1
      },
      "recipients": {
        "clicked": [
          {}
        ],
        "email": "ava@example.com",
        "opened": {
          "at": "string",
          "campaignId": "string",
          "subject": "string"
        },
        "unsubscribed": true
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.total` | number |  |
| `pagination.totalPages` | number |  |
| `recipients` | array<object> |  |
| `recipients.clicked` | array<object> |  |
| `recipients.email` | string |  |
| `recipients.opened` | array<object> |  |
| `recipients.opened.at` | string |  |
| `recipients.opened.campaignId` | string |  |
| `recipients.opened.subject` | string |  |
| `recipients.unsubscribed` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sequenzy API, this operation is `GET /metrics/recipients` (base URL `https://api.sequenzy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recipient-metrics-by-email.md) for the provider-specific parameters and requirements.

