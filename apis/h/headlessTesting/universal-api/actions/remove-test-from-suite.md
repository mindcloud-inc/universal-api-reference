# Headless Testing: Remove Test From Suite

Removes a test from a codeless suite in Headless Testing.

```
DELETE https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/remove-test-from-suite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/remove-test-from-suite?connectionId=$CONNECTION_ID&suiteId=string&testId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "suiteId": "string",
  "testId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/remove-test-from-suite?${params}`, {
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
| `suiteId` | string | yes | The codeless suite identifier. |
| `testId` | string | yes | The codeless test identifier in the suite. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true,
      "testId": 1
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
| `testId` | number |  |

## Native endpoint

Through the native Headless Testing API, this operation is `DELETE /labsuites/:suiteId/tests/:testId` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-test-from-suite.md) for the provider-specific parameters and requirements.

