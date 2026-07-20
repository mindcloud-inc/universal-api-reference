# xMatters: Upload attachment to a scenario

Uploads attachment to a scenario to your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/upload-attachment-to-a-scenario
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/upload-attachment-to-a-scenario" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/upload-attachment-to-a-scenario', {
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
| `file` | string | no |  |
| `fileName` | string | no |  |
| `formId` | string | no |  |
| `scenarioId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": {
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "path": "string",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links.self` | string |  |
| `name` | string |  |
| `path` | string |  |
| `size` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `POST forms/{formId}/scenarios/{scenarioId}/attachments` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-attachment-to-a-scenario.md) for the provider-specific parameters and requirements.

