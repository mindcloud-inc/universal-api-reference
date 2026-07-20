# Rulebricks: Create Rule Test

Creates a test for a Rulebricks rule.

```
POST https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/create-rule-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rulebricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/create-rule-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "critical": true,
  "name": "Ava Chen",
  "request": {},
  "response": {},
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/create-rule-test', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "critical": true,
    "name": "Ava Chen",
    "request": {},
    "response": {},
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `critical` | boolean | yes | Whether the test is critical |
| `name` | string | yes | Name of the test |
| `request` | object | yes | Request object for the test |
| `response` | object | yes | Expected response object for the test |
| `slug` | string | yes | Unique slug of the rule that will receive the new test |

## Response

```json
{
  "success": true,
  "data": [
    {
      "critical": true,
      "id": "string",
      "name": "Ava Chen",
      "request": {},
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `critical` | boolean | Whether the test is critical |
| `id` | string | Rule test ID |
| `name` | string | Rule test name |
| `request` | object | Rule test request object |
| `response` | object | Rule test response object |

## Native endpoint

Through the native Rulebricks API, this operation is `POST /admin/rules/:slug/tests` (base URL `https://rulebricks.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-rule-test.md) for the provider-specific parameters and requirements.

