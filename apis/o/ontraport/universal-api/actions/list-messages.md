# Ontraport: List Messages

Retrieves a list of messages from Ontraport.

```
GET https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ontraport `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/list-messages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "attachIcs": "string",
      "autosave": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "dateLastPublished": "2026-05-07T12:00:00.000Z",
      "dlm": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "id": "string",
      "isPublished": "string",
      "jsonData": "string",
      "lastAuto": "string",
      "lastSave": "string",
      "mcabuse": "string",
      "mcclicked": "string",
      "mcnotclicked": "string",
      "mcnotopened": "string",
      "mcopened": "string",
      "mcsent": "string",
      "mcunsub": "string",
      "messageBody": "string",
      "objectTypeId": "string",
      "oldResource": "string",
      "owner": "string",
      "plaintext": "string",
      "replyToEmail": "ava@example.com",
      "sendOutName": "Ava Chen",
      "sendTo": "string",
      "siteId": "string",
      "spamScore": "string",
      "subject": "string",
      "type": "string",
      "width": "string",
      "wordWrapCheckbox": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `attachIcs` | string |  |
| `autosave` | string |  |
| `date` | date |  |
| `dateLastPublished` | date |  |
| `dlm` | date |  |
| `from` | string |  |
| `id` | string |  |
| `isPublished` | string |  |
| `jsonData` | string |  |
| `lastAuto` | string |  |
| `lastSave` | string |  |
| `mcabuse` | string |  |
| `mcclicked` | string |  |
| `mcnotclicked` | string |  |
| `mcnotopened` | string |  |
| `mcopened` | string |  |
| `mcsent` | string |  |
| `mcunsub` | string |  |
| `messageBody` | string |  |
| `objectTypeId` | string |  |
| `oldResource` | string |  |
| `owner` | string |  |
| `plaintext` | string |  |
| `replyToEmail` | string |  |
| `sendOutName` | string |  |
| `sendTo` | string |  |
| `siteId` | string |  |
| `spamScore` | string |  |
| `subject` | string |  |
| `type` | string |  |
| `width` | string |  |
| `wordWrapCheckbox` | string |  |

## Native endpoint

Through the native Ontraport API, this operation is `GET /Messages` (base URL `https://api.ontraport.com/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

