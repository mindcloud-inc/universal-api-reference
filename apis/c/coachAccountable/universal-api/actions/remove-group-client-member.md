# CoachAccountable: Remove Group Client Member

Removes a group client member from CoachAccountable.

```
DELETE https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/remove-group-client-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/remove-group-client-member?connectionId=$CONNECTION_ID&groupClientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupClientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/remove-group-client-member?${params}`, {
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
| `groupClientId` | number | yes | The ID of the Group Client Member to be removed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoachAccountable API returns.

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-group-client-member.md) for the provider-specific parameters and requirements.

