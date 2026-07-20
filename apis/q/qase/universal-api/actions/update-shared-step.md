# Qase: Update shared step

Updates an existing shared step in Qase.

```
PUT https://connect.mindcloud.co/v1/universal/qase/latest/actions/update-shared-step
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qase/latest/actions/update-shared-step" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string",
  "hash": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qase/latest/actions/update-shared-step', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string",
    "hash": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | Code of project, where to search entities. |
| `hash` | string | yes | Hash. |
| `title` | string | yes | Required request field title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Qase API, this operation is `PATCH /shared_step/:code/:hash` (base URL `https://api.qase.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shared-step.md) for the provider-specific parameters and requirements.

