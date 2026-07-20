# Ontraport: Retrieve Specific Message

Retrieves a specific message from Ontraport.

```
GET https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-specific-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ontraport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-specific-message?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-specific-message?${params}`, {
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
| `id` | number | yes | The message ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
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
      "mcopened": "string",
      "mcsent": "string",
      "mcunsub": "string",
      "messageBody": "string",
      "objectTypeId": "string",
      "owner": "string",
      "plaintext": "string",
      "replyToEmail": "ava@example.com",
      "sendOutName": "Ava Chen",
      "sendTo": "string",
      "siteId": "string",
      "spamScore": "string",
      "subject": "string",
      "type": "string",
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
| `mcopened` | string |  |
| `mcsent` | string |  |
| `mcunsub` | string |  |
| `messageBody` | string |  |
| `objectTypeId` | string |  |
| `owner` | string |  |
| `plaintext` | string |  |
| `replyToEmail` | string |  |
| `sendOutName` | string |  |
| `sendTo` | string |  |
| `siteId` | string |  |
| `spamScore` | string |  |
| `subject` | string |  |
| `type` | string |  |
| `wordWrapCheckbox` | string |  |

## Native endpoint

Through the native Ontraport API, this operation is `GET /Message` (base URL `https://api.ontraport.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-specific-message.md) for the provider-specific parameters and requirements.

