# CoachAccountable: Update Action

Updates an action in CoachAccountable.

```
PUT https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/update-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/update-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/update-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionId` | number | yes |  |
| `theAction` | string | no |  |
| `dateDue` | date | no |  |
| `timeDue` | string | no |  |
| `timezoneOf` | list | no | Who's timezone the due date is in. Defaults to that of the assigning Coach. One of: `A`, `C`, `L`. |
| `projectName` | string | no | Name of the Project for the Aaction to be filed under. If set to "NULL" the Action will be changed to a standalone one. |
| `actionProjectId` | number | no | An alternative to projectName for specifying which project the Action should be filed under. |
| `weight` | number | no | Integer describing the relative significance of the Action within a project. Relevant only to Actions that are in a project. |
| `isLocked` | boolean | no | Prevent the Client from modifying or deleting the Action. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoachAccountable API returns.

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-action.md) for the provider-specific parameters and requirements.

