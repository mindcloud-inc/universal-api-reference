# SARE: Remove Subscribers From Groups By Email Address

Removes subscribers from SARE groups by email address.

```
PUT https://connect.mindcloud.co/v1/universal/sARE/latest/actions/remove-subscribers-from-groups-by-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SARE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sARE/latest/actions/remove-subscribers-from-groups-by-email-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "ava@example.com"
  ],
  "groups[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sARE/latest/actions/remove-subscribers-from-groups-by-email-address', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["ava@example.com"],
    "groups[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | yes | Subscriber email addresses to remove from the selected groups. |
| `groups[]` | array<number> | yes | Group identifiers that should lose the existing subscribers. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SARE API returns.

## Native endpoint

Through the native SARE API, this operation is `POST /group/remove_emails` (base URL `https://s.enewsletter.pl/api/v1/{{credentials.uid}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-subscribers-from-groups-by-email-address.md) for the provider-specific parameters and requirements.

