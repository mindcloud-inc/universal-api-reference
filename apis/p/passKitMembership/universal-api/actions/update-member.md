# PassKit Membership: Update Member

Updates an existing member in PassKit Membership.

```
PUT https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/update-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Membership `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/update-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/update-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `displayName` | string | no | Updated member display name. |
| `id` | string | yes | PassKit member id to update. |
| `points` | number | no | Updated points balance for the member. |
| `tierId` | string | no | Updated tier id for the member. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Updated PassKit member id. |

## Native endpoint

Through the native PassKit Membership API, this operation is `PUT /members/member` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-member.md) for the provider-specific parameters and requirements.

