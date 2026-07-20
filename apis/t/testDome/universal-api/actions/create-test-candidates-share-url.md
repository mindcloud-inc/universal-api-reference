# TestDome: Create Test Candidates Share URL

Creates a share URL for test candidates in TestDome.

```
POST https://connect.mindcloud.co/v1/universal/testDome/latest/actions/create-test-candidates-share-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/create-test-candidates-share-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "testId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testDome/latest/actions/create-test-candidates-share-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "testId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `testId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "shareUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | Dictionary |
| `shareUrl` | string | Shareable URL to access candidate reports on a test. |

## Native endpoint

Through the native TestDome API, this operation is `POST /tests/:testId/candidates/share-url` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-test-candidates-share-url.md) for the provider-specific parameters and requirements.

