# tl:dv: Import Meeting

Imports a meeting into tl:dv from a URL.

```
POST https://connect.mindcloud.co/v1/universal/tldv/latest/actions/import-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a tl:dv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tldv/latest/actions/import-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tldv/latest/actions/import-meeting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the meeting or recording being imported. |
| `url` | string | yes | The public URL of the meeting or recording to import. |
| `happenedAt` | date | no | The meeting or recording date and time. |
| `dryRun` | boolean | no | Run the import as a dry run without persisting it. |
| `participants[]` | array<string> | no | Invitee email addresses for the imported meeting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string | The tl;dv job identifier for the import request. |
| `message` | string | Provider message describing the import result. |
| `success` | boolean | Whether the import request was accepted. |

## Native endpoint

Through the native tl:dv API, this operation is `POST /v1alpha1/meetings/import` (base URL `https://pasta.tldv.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-meeting.md) for the provider-specific parameters and requirements.

