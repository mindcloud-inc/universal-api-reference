# Range: Delete Team Relation

Remove the relationship between a team and user.

```
DELETE https://connect.mindcloud.co/v1/universal/range/latest/actions/delete-team-relation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Range `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/range/latest/actions/delete-team-relation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/range/latest/actions/delete-team-relation?${params}`, {
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
| `teamId` | string | no | The team ID to update. |
| `userId` | string | no | The user ID to remove from the team relation. |

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
| `success` | boolean |  |

## Native endpoint

Through the native Range API, this operation is `DELETE /v1/teams/:teamId/relations/:userId` (base URL `https://api.range.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-team-relation.md) for the provider-specific parameters and requirements.

