# mittwald: Get Project Membership

Retrieves project membership from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-project-membership
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-project-membership?connectionId=$CONNECTION_ID&projectMembershipId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectMembershipId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-project-membership?${params}`, {
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
| `projectMembershipId` | string | yes | The unique identifier of the project membership. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "memberSince": "string",
      "projectId": "string",
      "role": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `memberSince` | string |  |
| `projectId` | string |  |
| `role` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/project-memberships/:projectMembershipId` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-membership.md) for the provider-specific parameters and requirements.

