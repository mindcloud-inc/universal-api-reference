# TestDome: Update Test URL

Updates an existing test URL in TestDome.

```
PUT https://connect.mindcloud.co/v1/universal/testDome/latest/actions/update-test-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/update-test-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "testId": 1,
  "testUrlId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testDome/latest/actions/update-test-url', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "testId": 1,
    "testUrlId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `disabled` | boolean | no |  |
| `testId` | number | yes |  |
| `testUrlId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TestDome API returns.

## Native endpoint

Through the native TestDome API, this operation is `PATCH /tests/:testId/urls/:testUrlId` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-test-url.md) for the provider-specific parameters and requirements.

