# Cursion: Generate Issue

Generates an issue from trigger data in Cursion.

```
POST https://connect.mindcloud.co/v1/universal/cursion/latest/actions/generate-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/generate-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "string",
  "triggerType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cursion/latest/actions/generate-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "string",
    "triggerType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | string | yes | The trigger resource ID. |
| `triggerType` | string | yes | The trigger type: scan, test, or caserun. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "affected": {},
      "details": "string",
      "id": "string",
      "labels": [
        "string"
      ],
      "status": "string",
      "time_created": "string",
      "title": "string",
      "trigger": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `affected` | object |  |
| `details` | string |  |
| `id` | string |  |
| `labels` | array<string> |  |
| `status` | string |  |
| `time_created` | string |  |
| `title` | string |  |
| `trigger` | object |  |

## Native endpoint

Through the native Cursion API, this operation is `POST /issue/generate` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-issue.md) for the provider-specific parameters and requirements.

