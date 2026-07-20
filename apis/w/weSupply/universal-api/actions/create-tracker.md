# WeSupply: Create Tracker

Creates a shipment tracker in WeSupply.

```
POST https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/create-tracker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/create-tracker" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/create-tracker', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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
| `message` | string | Tracker creation status message returned by WeSupply. |

## Native endpoint

Through the native WeSupply API, this operation is `POST /tracker/create` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tracker.md) for the provider-specific parameters and requirements.

