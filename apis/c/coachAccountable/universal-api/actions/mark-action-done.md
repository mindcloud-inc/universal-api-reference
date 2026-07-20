# CoachAccountable: Mark Action Done

Marks an action done in CoachAccountable.

```
PUT https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/mark-action-done
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/mark-action-done" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/mark-action-done', {
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
| `dateDone` | date | no | Optionally specify when the Action was completed, otherwise defaults to the time of the call. |
| `timeDone` | string | no | Optionally specify when the Action was completed, otherwise defaults to the time of the call. |
| `timezoneOf` | list | no | Who's timezone the date done is in. Defaults to that of the assigning Coach. One of: `A`, `C`, `L`. |
| `comment` | string | no | Optional comment to be posted on the Action as part of completing it. Will show as written by the assigning coach (or the client's primary coach if client-assigned). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoachAccountable API returns.

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-action-done.md) for the provider-specific parameters and requirements.

