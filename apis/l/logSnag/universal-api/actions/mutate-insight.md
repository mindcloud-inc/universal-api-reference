# LogSnag: Mutate Insight



```
PUT https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/mutate-insight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogSnag `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/mutate-insight" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "title": "string",
  "value": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/mutate-insight', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "string",
    "title": "string",
    "value": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | Project name in LogSnag. |
| `title` | string | yes | Insight title. |
| `value` | object | yes | Mutation object for the insight value. |
| `icon` | string | no | Single emoji or emoji shortcode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "icon": "string",
      "project": "string",
      "title": "string",
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `icon` | string | Rendered icon or emoji shortcode. |
| `project` | string | LogSnag project name. |
| `title` | string | Insight title. |
| `value` | object | Mutation object applied to the insight value. |

## Native endpoint

Through the native LogSnag API, this operation is `PATCH /insight` (base URL `https://api.logsnag.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mutate-insight.md) for the provider-specific parameters and requirements.

