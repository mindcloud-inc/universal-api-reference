# Switchur App: Set Switchboard Item Value



```
PUT https://connect.mindcloud.co/v1/universal/switchurApp/latest/actions/set-switchboard-item-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Switchur App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/switchurApp/latest/actions/set-switchboard-item-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "setToValue": "on"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/switchurApp/latest/actions/set-switchboard-item-value', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "setToValue": "on"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `setToValue` | string | yes | Value to set for the Switchboard item. For a switch, use on, off, or toggle; counters and keywords use the value accepted by the item type. Example: `on`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Switchur response message describing the updated item state |

## Native endpoint

Through the native Switchur App API, this operation is `PUT /:setToValue/{{credentials.switchboardItemToken}}` (base URL `https://api.switchur.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-switchboard-item-value.md) for the provider-specific parameters and requirements.

