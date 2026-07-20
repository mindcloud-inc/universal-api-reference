# Mendix: Remove Project Member

Removes a project team member from Mendix.

```
DELETE https://connect.mindcloud.co/v1/universal/mendix/latest/actions/remove-project-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mendix/latest/actions/remove-project-member?connectionId=$CONNECTION_ID&projectId=d92064a5-b1fd-4be4-97db-53fc90201d1c&userId=6f173f40-9e5d-4be0-b698-9ab965c0a31d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "d92064a5-b1fd-4be4-97db-53fc90201d1c",
  "userId": "6f173f40-9e5d-4be0-b698-9ab965c0a31d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendix/latest/actions/remove-project-member?${params}`, {
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
| `projectId` | string | yes | The unique identifier of a project. Example: `d92064a5-b1fd-4be4-97db-53fc90201d1c`. |
| `userId` | string | yes | The unique identifier of a user. Example: `6f173f40-9e5d-4be0-b698-9ab965c0a31d`. |

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
| `success` | boolean | Mendix documents no response body for this successful operation; this connector field represents request completion. |

## Native endpoint

Through the native Mendix API, this operation is `DELETE /projects/:projectId/members/:userId` (base URL `https://projects-api.home.mendix.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-project-member.md) for the provider-specific parameters and requirements.

