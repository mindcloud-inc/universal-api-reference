# PassKit Membership: Set Member Secondary Points By External ID

Updates a member's secondary points in PassKit Membership by external ID.

```
PUT https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/set-member-secondary-points-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Membership `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/set-member-secondary-points-by-external-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "externalId": "string",
  "programId": "string",
  "secondaryPoints": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/set-member-secondary-points-by-external-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "externalId": "string",
    "programId": "string",
    "secondaryPoints": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | yes | Member external id. |
| `programId` | string | yes | PassKit membership program id. |
| `secondaryPoints` | number | yes | Secondary points balance to set. |

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
| `id` | string |  |

## Native endpoint

Through the native PassKit Membership API, this operation is `PUT /members/member` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-member-secondary-points-by-external-id.md) for the provider-specific parameters and requirements.

