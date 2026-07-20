# Qase: Create test cases in bulk

Creates multiple test cases in Qase.

```
POST https://connect.mindcloud.co/v1/universal/qase/latest/actions/bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qase/latest/actions/bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string",
  "cases[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qase/latest/actions/bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string",
    "cases[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | Code of project, where to search entities. |
| `cases[]` | array<string> | yes | Required request field cases. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ids": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ids` | array<number> |  |

## Native endpoint

Through the native Qase API, this operation is `POST /case/:code/bulk` (base URL `https://api.qase.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk.md) for the provider-specific parameters and requirements.

