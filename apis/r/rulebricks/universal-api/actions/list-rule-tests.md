# Rulebricks: List Rule Tests

Retrieves tests for a Rulebricks rule.

```
GET https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/list-rule-tests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rulebricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/list-rule-tests?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/list-rule-tests?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | yes | Unique slug of the rule whose tests should be listed |

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

Through the native Rulebricks API, this operation is `GET /admin/rules/:slug/tests` (base URL `https://rulebricks.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rule-tests.md) for the provider-specific parameters and requirements.

