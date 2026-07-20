# Headless Testing: Update Suite Browsers

Updates browser assignments for a codeless suite in Headless Testing.

```
PUT https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-suite-browsers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-suite-browsers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "browser_ids": "string",
  "suiteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-suite-browsers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "browser_ids": "string",
    "suiteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `browser_ids` | string | yes | Comma-separated browser IDs to assign to the codeless suite. |
| `suiteId` | string | yes | The codeless suite identifier. |

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

Through the native Headless Testing API, this operation is `POST /labsuites/:suiteId/browsers` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-suite-browsers.md) for the provider-specific parameters and requirements.

