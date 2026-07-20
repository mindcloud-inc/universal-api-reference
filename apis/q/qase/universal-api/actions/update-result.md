# Qase: Update test run result

Updates an existing test run result in Qase.

```
PUT https://connect.mindcloud.co/v1/universal/qase/latest/actions/update-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qase/latest/actions/update-result" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string",
  "id": 1,
  "hash": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qase/latest/actions/update-result', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string",
    "id": 1,
    "hash": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | Code of project, where to search entities. |
| `status` | string | no | Updated result status. |
| `id` | number | yes | Identifier. |
| `hash` | string | yes | Hash. |

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

Through the native Qase API, this operation is `PATCH /result/:code/:id/:hash` (base URL `https://api.qase.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-result.md) for the provider-specific parameters and requirements.

