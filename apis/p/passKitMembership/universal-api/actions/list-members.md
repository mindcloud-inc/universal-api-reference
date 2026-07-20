# PassKit Membership: List Members

Retrieves members from a PassKit Membership program.

```
GET https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Membership `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/list-members?connectionId=$CONNECTION_ID&limit=25&offset=0&programId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "programId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/list-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `programId` | string | yes | PassKit Program ID from the target membership program settings page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "externalId": "string",
      "id": "string",
      "optOut": true,
      "points": 1,
      "profileImage": "string",
      "programId": "string",
      "secondaryPoints": 1,
      "status": "string",
      "tierId": "string",
      "tierPoints": 1,
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string | Member creation timestamp. |
| `externalId` | string | External member identifier. |
| `id` | string | PassKit member identifier. |
| `optOut` | boolean | Whether the member has opted out. |
| `points` | number | Primary points balance. |
| `profileImage` | string | Profile image reference. |
| `programId` | string | Parent membership program identifier. |
| `secondaryPoints` | number | Secondary points balance. |
| `status` | string | Member enrolment status. |
| `tierId` | string | Current membership tier identifier. |
| `tierPoints` | number | Tier points balance. |
| `updated` | string | Member update timestamp. |

## Native endpoint

Through the native PassKit Membership API, this operation is `POST /members/member/list/:programId` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

