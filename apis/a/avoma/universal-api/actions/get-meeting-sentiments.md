# Avoma: Get Meeting Sentiments

Retrieves sentiments for a meeting from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-meeting-sentiments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-meeting-sentiments?connectionId=$CONNECTION_ID&meetingUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meetingUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-meeting-sentiments?${params}`, {
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
| `meetingUuid` | string | yes | Unique ID of the meeting for which sentiments will be fetched. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sentiment": 1,
      "sentimentRanges": [
        {
          "score": 1,
          "timeRange": [
            1
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sentiment` | number |  |
| `sentimentRanges[].score` | number |  |
| `sentimentRanges[].timeRange[]` | number |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/meeting_sentiments/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting-sentiments.md) for the provider-specific parameters and requirements.

