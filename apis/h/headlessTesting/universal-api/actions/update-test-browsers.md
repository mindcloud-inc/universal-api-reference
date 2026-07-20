# Headless Testing: Update Test Browsers

Updates browser assignments for a codeless test in Headless Testing.

```
PUT https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-test-browsers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-test-browsers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "browser_ids": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-test-browsers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "browser_ids": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `browser_ids` | string | yes | Comma-separated browser IDs to assign to the codeless test. |
| `id` | string | yes | The codeless test identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browserCount": 1,
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
| `browserCount` | number |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Headless Testing API, this operation is `POST /lab/:id/browsers` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-test-browsers.md) for the provider-specific parameters and requirements.

