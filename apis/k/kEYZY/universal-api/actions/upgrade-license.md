# KEYZY: Upgrade License

Upgrades a KEYZY license from another license.

```
PUT https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/upgrade-license
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KEYZY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/upgrade-license" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currentSerial": "string",
  "upgradeSerial": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/upgrade-license', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currentSerial": "string",
    "upgradeSerial": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currentSerial` | string | yes | Current license serial number. |
| `upgradeSerial` | string | yes | Upgrade license serial number. |

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
| `message` | string | Upgrade confirmation message. |

## Native endpoint

Through the native KEYZY API, this operation is `POST /licenses/upgrade` (base URL `https://api.keyzy.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upgrade-license.md) for the provider-specific parameters and requirements.

