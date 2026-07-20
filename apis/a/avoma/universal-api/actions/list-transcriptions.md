# Avoma: List Transcriptions

Retrieves transcriptions from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-transcriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-transcriptions?connectionId=$CONNECTION_ID&fromDate=string&toDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "string",
  "toDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/list-transcriptions?${params}`, {
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
| `fromDate` | string | yes | Retrieve transcriptions for meetings started at or after this UTC datetime. Use ISO 8601 unless meeting UUID is provided. |
| `toDate` | string | yes | Retrieve transcriptions for meetings started at or before this UTC datetime. Use ISO 8601 unless meeting UUID is provided. |
| `meetingUuid` | string | no | Unique ID of the meeting for which transcriptions will be fetched. |
| `page` | number | no | Page number for pagination when meeting UUID is not provided. |
| `pageSize` | number | no | Number of items per page when meeting UUID is not provided. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meetingUuid": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "speakers": [
        {
          "email": "ava@example.com",
          "id": 1,
          "isRep": true,
          "name": "Ava Chen"
        }
      ],
      "transcript": [
        {
          "speakerId": 1,
          "timestamps": [
            1
          ],
          "transcript": "string"
        }
      ],
      "transcriptionVttUrl": "https://example.com",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meetingUuid` | string |  |
| `modified` | date |  |
| `speakers[].email` | string |  |
| `speakers[].id` | number |  |
| `speakers[].isRep` | boolean |  |
| `speakers[].name` | string |  |
| `transcript[].speakerId` | number |  |
| `transcript[].timestamps[]` | number |  |
| `transcript[].transcript` | string |  |
| `transcriptionVttUrl` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/transcriptions/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transcriptions.md) for the provider-specific parameters and requirements.

