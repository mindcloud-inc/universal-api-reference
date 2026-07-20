# BunnyCDN: Check Pull Zone Availability

Checks pull zone availability in BunnyCDN.

```
POST https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/check-pull-zone-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/check-pull-zone-availability" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/check-pull-zone-availability', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Pull zone name to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Available": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Available` | boolean | Whether the pull zone name is available. |

## Native endpoint

Through the native BunnyCDN API, this operation is `POST /pullzone/checkavailability` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-pull-zone-availability.md) for the provider-specific parameters and requirements.

