# Cursion: Create Issue



```
POST https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "affected": {},
  "details": "string",
  "title": "string",
  "trigger": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "affected": {},
    "details": "string",
    "title": "string",
    "trigger": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `affected` | object | yes | The affected resource object with id, str, and type. |
| `details` | string | yes | The issue details in Markdown. |
| `title` | string | yes | The issue title. |
| `trigger` | object | yes | The trigger object with id and type. |

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

Through the native Cursion API, this operation is `POST /issue` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-issue.md) for the provider-specific parameters and requirements.

