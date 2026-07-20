# CloudContactAI: List Messages by Campaign



```
GET https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/list-messages-by-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/list-messages-by-campaign?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/list-messages-by-campaign?${params}`, {
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
| `campaignId` | string | no | The campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": 1,
      "contactFirstName": "Ava",
      "contactLastName": "Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isArchived": true,
      "message": "string",
      "phone": "string",
      "segments": 1,
      "sentAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "twilioErrorCode": "string",
      "twilioErrorMessage": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userClientId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | number |  |
| `contactFirstName` | string |  |
| `contactLastName` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `message` | string |  |
| `phone` | string |  |
| `segments` | number |  |
| `sentAt` | date |  |
| `status` | string |  |
| `twilioErrorCode` | string |  |
| `twilioErrorMessage` | string |  |
| `updatedAt` | date |  |
| `userClientId` | string |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `GET api/v2/messages/campaign/:campaignId` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages-by-campaign.md) for the provider-specific parameters and requirements.

