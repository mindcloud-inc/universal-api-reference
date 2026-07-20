# Campaign Monitor: Update List

Updates an existing list in Campaign Monitor.

```
PUT https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/update-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/update-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/update-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | Campaign Monitor list identifier. |
| `title` | string | no | Title of the list. |
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
| `response` | string | Empty string on success because Campaign Monitor returns HTTP 200 OK with no response body for list updates. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `PUT /lists/:listId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-list.md) for the provider-specific parameters and requirements.

