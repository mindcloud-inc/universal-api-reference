# Campaign Monitor: Create List

Creates a new list in Campaign Monitor.

```
POST https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | Campaign Monitor client identifier. |
| `title` | string | yes | Title of the list. |
| `unsubscribePage` | string | no | URL for the list unsubscribe page. |
| `confirmedOptIn` | boolean | no | Whether the list requires confirmed opt-in. |
| `confirmationSuccessPage` | string | no | URL used after confirmation succeeds. |
| `unsubscribeSetting` | string | no | Campaign Monitor unsubscribe behavior for the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | List ID returned by Campaign Monitor when the list is created. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `POST /lists/:clientId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

