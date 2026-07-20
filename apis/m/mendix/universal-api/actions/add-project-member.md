# Mendix: Add Project Member

Adds a project team member in Mendix or sends an invitation.

```
POST https://connect.mindcloud.co/v1/universal/mendix/latest/actions/add-project-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/add-project-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "d92064a5-b1fd-4be4-97db-53fc90201d1c"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mendix/latest/actions/add-project-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "d92064a5-b1fd-4be4-97db-53fc90201d1c"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The unique identifier of a project. Example: `d92064a5-b1fd-4be4-97db-53fc90201d1c`. |
| `memberId` | string | no | Unique identifier of the member to add to the project. Example: `6f173f40-9e5d-4be0-b698-9ab965c0a31d`. |
| `roleId` | string | no | The unique identifier of the role assigned to the member. Example: `fdea56de-3c79-48d9-93ff-61cbc736426c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Mendix documents a successful no-body create or accepted response; this connector field represents request completion. |

## Native endpoint

Through the native Mendix API, this operation is `POST /projects/:projectId/members` (base URL `https://projects-api.home.mendix.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-project-member.md) for the provider-specific parameters and requirements.

