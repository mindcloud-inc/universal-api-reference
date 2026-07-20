# CoachAccountable: Delete Action Project

Deletes an action project from CoachAccountable.

```
DELETE https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/delete-action-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/delete-action-project?connectionId=$CONNECTION_ID&clientId=1&actionProjectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "1",
  "actionProjectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/delete-action-project?${params}`, {
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
| `clientId` | number | yes |  |
| `actionProjectId` | number | yes | The ID of the Project you wish to delete. |
| `keepActions` | boolean | no | Keep Actions within a Project around as standalone Actions. If false, delete any Actions within the Project. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoachAccountable API returns.

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-action-project.md) for the provider-specific parameters and requirements.

