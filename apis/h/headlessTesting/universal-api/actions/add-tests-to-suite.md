# Headless Testing: Add Tests To Suite

Adds tests to a codeless suite in Headless Testing.

```
POST https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/add-tests-to-suite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/add-tests-to-suite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "suiteId": "string",
  "test_ids": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/add-tests-to-suite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "suiteId": "string",
    "test_ids": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `suiteId` | string | yes | The codeless suite identifier. |
| `test_ids` | string | yes | Comma-separated codeless test IDs to add to the suite. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true,
      "suiteId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |
| `suiteId` | number |  |

## Native endpoint

Through the native Headless Testing API, this operation is `POST /labsuites/:suiteId/tests` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tests-to-suite.md) for the provider-specific parameters and requirements.

