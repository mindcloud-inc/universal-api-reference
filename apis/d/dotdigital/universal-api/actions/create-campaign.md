# Dotdigital: Create Campaign

Creates a new campaign in Dotdigital.

```
POST https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dotdigital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "subject": "string",
  "fromName": "Ava Chen",
  "htmlContent": "string",
  "plainTextContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dotdigital/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "subject": "string",
    "fromName": "Ava Chen",
    "htmlContent": "string",
    "plainTextContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the campaign being created |
| `subject` | string | yes | The email subject line of the campaign |
| `fromName` | string | yes | The from name of the campaign |
| `htmlContent` | string | yes | The HTML content of the campaign |
| `plainTextContent` | string | yes | The plain text content of the campaign |
| `fromAddress.email` | string | no |  |
| `fromAddress.id` | number | no |  |
| `replyAction` | string | no |  |
| `replyToAddress` | string | no |  |
| `type` | list<string> | no | One of: `Standard`, `Triggered`. |

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
      "status": "string",
      "subject": "string",
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
| `status` | string |  |
| `subject` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dotdigital API, this operation is `POST /v2/campaigns` (base URL `https://r2-api.dotmailer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

