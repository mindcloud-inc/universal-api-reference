# Dotdigital: Get Campaign With Details

Retrieves a campaign and its details from Dotdigital.

```
GET https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-campaign-with-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotdigital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-campaign-with-details?connectionId=$CONNECTION_ID&id=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/get-campaign-with-details?${params}`, {
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
| `id` | number | yes | The ID of the campaign. Example: `12345`. |

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
      "splitTestOptions": [
        "string"
      ],
      "status": "string",
      "subject": "string",
      "tags": [
        "string"
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
| `splitTestOptions` | array<string> |  |
| `status` | string |  |
| `subject` | string |  |
| `tags` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native Dotdigital API, this operation is `GET /v2/campaigns/:id/with-details` (base URL `https://r2-api.dotmailer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-with-details.md) for the provider-specific parameters and requirements.

