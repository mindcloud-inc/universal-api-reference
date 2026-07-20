# TestDome: Delete Test

Deletes an existing test from TestDome.

```
DELETE https://connect.mindcloud.co/v1/universal/testDome/latest/actions/delete-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/delete-test?connectionId=$CONNECTION_ID&testId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "testId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testDome/latest/actions/delete-test?${params}`, {
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
| `testId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TestDome API returns.

## Native endpoint

Through the native TestDome API, this operation is `DELETE /tests/:testId` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-test.md) for the provider-specific parameters and requirements.

