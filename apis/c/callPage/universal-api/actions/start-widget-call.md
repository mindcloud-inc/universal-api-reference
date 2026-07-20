# CallPage: Start Widget Call

Starts a widget call in CallPage.

```
POST https://connect.mindcloud.co/v1/universal/callPage/latest/actions/start-widget-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/start-widget-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "widgetId": "123",
  "tel": "+15551234567"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callPage/latest/actions/start-widget-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "widgetId": "123",
    "tel": "+15551234567"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `widgetId` | number | yes | Widget identifier. Example: `123`. |
| `tel` | string | yes | Phone number to call in E.164 format. Example: `+15551234567`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `departmentId` | number | no | Optional department identifier. Example: `42`. |
| `managerId` | number | no | Optional manager identifier. Example: `100447`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | The created call identifier. |

## Native endpoint

Through the native CallPage API, this operation is `POST /widgets/call` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-widget-call.md) for the provider-specific parameters and requirements.

