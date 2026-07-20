# Amberscript: Export JSON

Retrieves JSON export for an Amberscript job.

```
GET https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/export-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amberscript `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/export-json?connectionId=$CONNECTION_ID&jobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/export-json?${params}`, {
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
| `jobId` | string | yes | The finished job to export. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "id": "string",
      "recordId": "string",
      "segments": [
        {
          "speaker": "string",
          "words": [
            {
              "conf": 1,
              "duration": 1,
              "end": 1,
              "pristine": true,
              "start": 1,
              "text": "string"
            }
          ]
        }
      ],
      "speakers": [
        {
          "name": "Ava Chen",
          "spkid": "string"
        }
      ],
      "startTimeOffset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string |  |
| `id` | string |  |
| `recordId` | string |  |
| `segments[].speaker` | string |  |
| `segments[].words[].conf` | number |  |
| `segments[].words[].duration` | number |  |
| `segments[].words[].end` | number |  |
| `segments[].words[].pristine` | boolean |  |
| `segments[].words[].start` | number |  |
| `segments[].words[].text` | string |  |
| `speakers[].name` | string |  |
| `speakers[].spkid` | string |  |
| `startTimeOffset` | number |  |

## Native endpoint

Through the native Amberscript API, this operation is `GET /jobs/export-json` (base URL `https://api.amberscript.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-json.md) for the provider-specific parameters and requirements.

