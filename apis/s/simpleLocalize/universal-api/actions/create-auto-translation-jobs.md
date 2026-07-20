# SimpleLocalize: Create Auto-Translation Jobs

Creates auto-translation jobs in SimpleLocalize.

```
POST https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/create-auto-translation-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleLocalize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/create-auto-translation-jobs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/create-auto-translation-jobs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageKeys[]` | array<string> | no | Project source language keys, if not provided then all languages will be translated. Auto-translation configuration will be used from the last auto-translation job. |
| `options` | list<string> | no | Options for auto-translation One of: `FORCE_REPLACE`, `USE_TRANSLATION_KEYS`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "message": "string",
      "metadata": {},
      "progress": 1,
      "started": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string |  |
| `message` | string |  |
| `metadata` | object |  |
| `progress` | number |  |
| `started` | date |  |
| `state` | string |  |
| `type` | string |  |

## Native endpoint

Through the native SimpleLocalize API, this operation is `POST /api/v2/jobs/auto-translate` (base URL `https://api.simplelocalize.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-auto-translation-jobs.md) for the provider-specific parameters and requirements.

