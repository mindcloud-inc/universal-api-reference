# Dotdigital: Get All Campaigns With Filters

Retrieves campaigns from Dotdigital with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-all-campaigns-with-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotdigital `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-all-campaigns-with-filters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-all-campaigns-with-filters?${params}`, {
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
| `type` | list<string> | no | One of: `Standard`, `Triggered`. |
| `tags` | string | no | Only campaigns that contain all supplied tags are returned. Accepts multiple values in one string, delimited by `,`. Example: `welcome`. |
| `sentDate` | date | no | Return campaigns sent on or after this UTC ISO-8601 date-time. Example: `2026-03-01`. |
| `statuses` | list<string> | no | Allowed values: Unsent, Sent, Sending, Paused, Cancelled, RequiresWorkflowApproval. One of: `Cancelled`, `Paused`, `RequiresWorkflowApproval`, `Sending`, `Sent`, `Unsent`. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customReplyToAddress": "string",
      "fromAddress": {
        "email": "ava@example.com",
        "id": 1
      },
      "fromName": "Ava Chen",
      "htmlContent": "string",
      "id": 1,
      "isSplitTest": true,
      "name": "Ava Chen",
      "plainTextContent": "string",
      "replyAction": "string",
      "replyToAddress": "string",
      "sentDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subject": "string",
      "tags": [
        [
          "string"
        ]
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customReplyToAddress` | string |  |
| `fromAddress` | object |  |
| `fromAddress.email` | string |  |
| `fromAddress.id` | number |  |
| `fromName` | string |  |
| `htmlContent` | string |  |
| `id` | number |  |
| `isSplitTest` | boolean |  |
| `name` | string |  |
| `plainTextContent` | string |  |
| `replyAction` | string |  |
| `replyToAddress` | string |  |
| `sentDate` | date |  |
| `status` | string |  |
| `subject` | string |  |
| `tags[]` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native Dotdigital API, this operation is `GET /v2/campaigns/filtered` (base URL `https://r2-api.dotmailer.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-all-campaigns-with-filters.md) for the provider-specific parameters and requirements.

