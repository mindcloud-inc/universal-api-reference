# PassKit Membership: Create Member

Creates a member in PassKit Membership.

```
POST https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/create-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Membership `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/create-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "displayName": "Ava Chen",
  "externalId": "string",
  "programId": "string",
  "tierId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/create-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "displayName": "Ava Chen",
    "externalId": "string",
    "programId": "string",
    "tierId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `displayName` | string | yes | Display name for the enrolled member. |
| `externalId` | string | yes | External member identifier used to de-duplicate enrolments. |
| `programId` | string | yes | PassKit membership program identifier. |
| `tierId` | string | yes | PassKit membership tier identifier. |

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
| `id` | string | Created PassKit member identifier. |

## Native endpoint

Through the native PassKit Membership API, this operation is `POST /members/member` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-member.md) for the provider-specific parameters and requirements.

