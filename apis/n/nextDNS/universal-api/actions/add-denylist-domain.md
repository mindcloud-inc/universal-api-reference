# NextDNS: Add Denylist Domain

Creates a denylist domain entry in a NextDNS profile.

```
POST https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/add-denylist-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextDNS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/add-denylist-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/add-denylist-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileId` | string | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
| `id` | string | yes | Domain to add to the denylist. |
| `active` | boolean | no | Whether the denylist entry is active. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NextDNS API returns.

## Native endpoint

Through the native NextDNS API, this operation is `POST /profiles/:profile/denylist` (base URL `https://api.nextdns.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-denylist-domain.md) for the provider-specific parameters and requirements.

