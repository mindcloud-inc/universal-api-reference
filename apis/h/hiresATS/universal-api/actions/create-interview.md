# 100Hires ATS: Create Interview

Schedules an interview for an application in 100Hires ATS.

```
POST https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/create-interview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 100Hires ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/create-interview" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "4806315",
  "startTime": "1774554000",
  "endTime": "1774557600",
  "interviewerIds[]": "35586"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hiresATS/latest/actions/create-interview', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "4806315",
    "startTime": "1774554000",
    "endTime": "1774557600",
    "interviewerIds[]": "35586"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Application ID to attach the interview to. Example: `4806315`. |
| `startTime` | number | yes | Interview start time as a Unix timestamp in seconds. Example: `1774554000`. |
| `endTime` | number | yes | Interview end time as a Unix timestamp in seconds. Example: `1774557600`. |
| `interviewerIds[]` | array<number> | yes | User IDs for the interviewers. Example: `35586`. |
| `location` | string | no | Optional interview location string. Example: `Google Meet`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Comma-separated related interview resources to include. Example: `candidate,interviewers`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 100Hires ATS API returns.

## Native endpoint

Through the native 100Hires ATS API, this operation is `POST /applications/:id/interviews` (base URL `https://api.100hires.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-interview.md) for the provider-specific parameters and requirements.

