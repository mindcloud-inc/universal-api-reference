# TestDome: Create Test URL

Creates a new test URL in TestDome.

```
POST https://connect.mindcloud.co/v1/universal/testDome/latest/actions/create-test-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/create-test-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "testId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testDome/latest/actions/create-test-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "testId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `testId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "candidatesCompleted": 1,
      "disabled": true,
      "id": 1,
      "key": "string",
      "modified": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | Dictionary |
| `candidatesCompleted` | number | The amount of candidates that completed the test using the test URL. |
| `disabled` | boolean | Determines if the test URL is disabled. |
| `id` | number | The ID of the test URL. |
| `key` | string | The unique string that composes the test URL. |
| `modified` | string | The time the URL was last modified. |
| `name` | string | The name of the test URL. |

## Native endpoint

Through the native TestDome API, this operation is `POST /tests/:testId/urls` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-test-url.md) for the provider-specific parameters and requirements.

