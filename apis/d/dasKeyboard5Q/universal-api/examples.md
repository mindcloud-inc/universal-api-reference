# Das Keyboard 5Q Universal API Examples

These examples use the MindCloud API key and Das Keyboard 5Q connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Signals

Retrieves signals from Das Keyboard 5Q.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/list-signals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/list-signals?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "clientName": "Ava Chen",
      "color": "string",
      "createdAt": 1,
      "effect": "string",
      "id": 1,
      "isArchived": true,
      "isMuted": true,
      "isRead": true,
      "message": "string",
      "name": "Ava Chen",
      "pid": "string",
      "updatedAt": 1,
      "userId": 1,
      "zoneId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Signals action reference](actions/list-signals.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dasKeyboard5Q/latest/actions/list-signals).

## Create Signal

Creates a signal in Das Keyboard 5Q.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/create-signal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Apple Stock Increase",
  "zoneId": "KEY_Q",
  "color": "#FF0000",
  "pid": "DK5QPID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/create-signal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Apple Stock Increase",
    "zoneId": "KEY_Q",
    "color": "#FF0000",
    "pid": "DK5QPID"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "clientName": "Ava Chen",
      "color": "string",
      "createdAt": 1,
      "effect": "string",
      "id": 1,
      "isArchived": true,
      "isMuted": true,
      "isRead": true,
      "message": "string",
      "name": "Ava Chen",
      "pid": "string",
      "updatedAt": 1,
      "userId": 1,
      "zoneId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Signal action reference](actions/create-signal.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dasKeyboard5Q/latest/actions/create-signal).
