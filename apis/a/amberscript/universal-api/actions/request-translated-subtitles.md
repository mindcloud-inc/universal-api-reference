# Amberscript: Request Translated Subtitles

Requests translated subtitles for an existing Amberscript manual captions job.

```
POST https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/request-translated-subtitles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amberscript `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/request-translated-subtitles" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceJobId": "string",
  "targetLanguage": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/request-translated-subtitles', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceJobId": "string",
    "targetLanguage": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceJobId` | string | yes | Existing manual captions job to translate. |
| `targetLanguage` | string | yes | Target language code for the translated subtitles job. |
| `turnaroundTime` | string | no | Optional turnaround time for the translated subtitles job. Default: `SEVEN_DAYS`. |
| `callbackUrl` | string | no | Optional webhook URL for final job status callbacks. |
| `notes` | string | no | Optional notes for the translated subtitles job. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amberscript API returns.

## Native endpoint

Through the native Amberscript API, this operation is `POST /jobs/translatedSubtitles` (base URL `https://api.amberscript.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-translated-subtitles.md) for the provider-specific parameters and requirements.

