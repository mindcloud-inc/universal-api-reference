# WeBeHome: Set Switch Status



```
PUT https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/set-switch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeBeHome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/set-switch-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "BaseUnitID": "18993",
  "SubUnitID": "0",
  "Status": "99"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/set-switch-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "BaseUnitID": "18993",
    "SubUnitID": "0",
    "Status": "99"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `BaseUnitID` | string | yes | Base unit ID. Default: `18993`. |
| `SubUnitID` | string | yes | Sub unit ID. Default: `0`. |
| `Status` | string | yes | 0=off, 1-98 dim level, 99=on. Default: `99`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | string |  |

## Native endpoint

Through the native WeBeHome API, this operation is `GET WebAPI.aspx` (base URL `https://webehome.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-switch-status.md) for the provider-specific parameters and requirements.

