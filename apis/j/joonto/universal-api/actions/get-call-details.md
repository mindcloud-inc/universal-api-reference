# Joonto: Get Call Details



```
GET https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-call-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Joonto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-call-details?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-call-details?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callerId": "string",
      "callerName": "Ava Chen",
      "callStatus": "string",
      "callStreamUrl": "https://example.com",
      "callType": "string",
      "conferenceSid": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "dtmfLog": "string",
      "duration": 1,
      "endTime": "2026-05-07T12:00:00.000Z",
      "forwardFrom": "string",
      "from": "string",
      "fromEmail": "ava@example.com",
      "fromImageId": 1,
      "fromName": "Ava Chen",
      "fromPretty": "string",
      "id": 1,
      "managerSid": "string",
      "originalFrom": "string",
      "originalTo": "string",
      "plan": "string",
      "price": 1,
      "record": "string",
      "recordingUrl": "https://example.com",
      "secondarySid": "string",
      "sid": "string",
      "startTime": "2026-05-07T12:00:00.000Z",
      "strDuration": "string",
      "to": "string",
      "toEmail": "ava@example.com",
      "toImageId": 1,
      "toName": "Ava Chen",
      "toPretty": "string",
      "transcription": "string",
      "transcriptionLog": "string",
      "userId": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callerId` | string |  |
| `callerName` | string |  |
| `callStatus` | string |  |
| `callStreamUrl` | string |  |
| `callType` | string |  |
| `conferenceSid` | string |  |
| `dateCreated` | date |  |
| `direction` | string |  |
| `dtmfLog` | string |  |
| `duration` | number |  |
| `endTime` | date |  |
| `forwardFrom` | string |  |
| `from` | string |  |
| `fromEmail` | string |  |
| `fromImageId` | number |  |
| `fromName` | string |  |
| `fromPretty` | string |  |
| `id` | number |  |
| `managerSid` | string |  |
| `originalFrom` | string |  |
| `originalTo` | string |  |
| `plan` | string |  |
| `price` | number |  |
| `record` | string |  |
| `recordingUrl` | string |  |
| `secondarySid` | string |  |
| `sid` | string |  |
| `startTime` | date |  |
| `strDuration` | string |  |
| `to` | string |  |
| `toEmail` | string |  |
| `toImageId` | number |  |
| `toName` | string |  |
| `toPretty` | string |  |
| `transcription` | string |  |
| `transcriptionLog` | string |  |
| `userId` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Joonto API, this operation is `GET /api/Calls/Get/:id` (base URL `https://api.joonto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-details.md) for the provider-specific parameters and requirements.

