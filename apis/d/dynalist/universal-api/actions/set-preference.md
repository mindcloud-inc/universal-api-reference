# Dynalist: Set Preference

Updates a preference value in Dynalist.

```
PUT https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/set-preference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynalist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/set-preference" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "key": "string",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/set-preference', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "key": "string",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | yes | Preference key to update. |
| `value` | string | yes | New preference value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_code": "string",
      "_msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_code` | string |  |
| `_msg` | string |  |

## Native endpoint

Through the native Dynalist API, this operation is `POST /pref/set` (base URL `https://dynalist.io/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-preference.md) for the provider-specific parameters and requirements.

