# PassKit Membership: Find Member By External ID

Finds a member in PassKit Membership by external ID.

```
GET https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/find-member-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Membership `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/find-member-by-external-id?connectionId=$CONNECTION_ID&memberId=string&programId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "memberId": "string",
  "programId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/find-member-by-external-id?${params}`, {
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
| `memberId` | string | yes | Member external id to look up. |
| `programId` | string | yes | PassKit program id to search within. |

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
| `created` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `optOut` | boolean |  |
| `points` | number |  |
| `profileImage` | string |  |
| `programId` | string |  |
| `secondaryPoints` | number |  |
| `status` | string |  |
| `tierId` | string |  |
| `tierPoints` | number |  |
| `updated` | string |  |

## Native endpoint

Through the native PassKit Membership API, this operation is `POST /members/member/list/:programId` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-member-by-external-id.md) for the provider-specific parameters and requirements.

