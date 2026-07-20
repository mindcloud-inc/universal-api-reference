# Maildrip: Restore draft email to editing



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/restore-draft-email-to-editing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/restore-draft-email-to-editing?connectionId=$CONNECTION_ID&campaignId=string&emailId=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string",
  "emailId": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/restore-draft-email-to-editing?${params}`, {
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
| `campaignId` | string | yes | ID of the campaign |
| `emailId` | string | yes | ID of the draft email |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__v": 1,
      "_id": "string",
      "assets": [
        "string"
      ],
      "attachments": [
        "string"
      ],
      "body": "string",
      "campaign": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultAssets": [
        "string"
      ],
      "groups": [
        "string"
      ],
      "groupType": [
        "string"
      ],
      "status": 1,
      "subject": "string",
      "title": "string",
      "typeOfMail": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": "string",
      "x_processed_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__v` | number |  |
| `_id` | string |  |
| `assets` | array<string> |  |
| `attachments` | array<string> |  |
| `body` | string |  |
| `campaign` | string |  |
| `createdAt` | date |  |
| `defaultAssets` | array<string> |  |
| `groups` | array<string> |  |
| `groupType` | array<string> |  |
| `status` | number |  |
| `subject` | string |  |
| `title` | string |  |
| `typeOfMail` | string |  |
| `updatedAt` | date |  |
| `user` | string |  |
| `x_processed_status` | string |  |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/campaigns/{campaignId}/{emailId}/restore-mail-to-editing` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-draft-email-to-editing.md) for the provider-specific parameters and requirements.

