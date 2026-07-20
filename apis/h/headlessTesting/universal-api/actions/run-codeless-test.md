# Headless Testing: Run Codeless Test

Runs a codeless test in Headless Testing.

```
POST https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/run-codeless-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/run-codeless-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/run-codeless-test', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The codeless test identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobId` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Headless Testing API, this operation is `POST /lab/:id/trigger` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-codeless-test.md) for the provider-specific parameters and requirements.

