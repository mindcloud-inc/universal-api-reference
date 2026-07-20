# Qase: Create test run result

Creates a test run result in Qase.

```
POST https://connect.mindcloud.co/v1/universal/qase/latest/actions/create-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qase/latest/actions/create-result" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string",
  "id": 1,
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qase/latest/actions/create-result', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string",
    "id": 1,
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | Code of project, where to search entities. |
| `id` | number | yes | Identifier. |
| `status` | string | yes | Can have the following values `passed`, `failed`, `blocked`, `skipped`, `invalid` + custom statuses |

## Response

```json
{
  "success": true,
  "data": [
    {
      "case_id": 1,
      "hash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `case_id` | number |  |
| `hash` | string |  |

## Native endpoint

Through the native Qase API, this operation is `POST /result/:code/:id` (base URL `https://api.qase.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-result.md) for the provider-specific parameters and requirements.

