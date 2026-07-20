# SuperSend: Export Placement Tests

Creates a placement test export in SuperSend.

```
POST https://connect.mindcloud.co/v1/universal/superSend/latest/actions/export-placement-tests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/export-placement-tests" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/export-placement-tests', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes |  |
| `filters` | object | no |  |
| `filters.search` | string | no |  |
| `filters.status` | string | no |  |
| `filters.conditionalFilters` | string | no |  |
| `filters.sortBy` | string | no |  |
| `filters.sortOrder` | string | no | Allowed values: asc, desc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "request_id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `request_id` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native SuperSend API, this operation is `POST /placement-tests/export` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-placement-tests.md) for the provider-specific parameters and requirements.

