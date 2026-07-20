# OnePlan: List Workplan Fragments

Retrieves workplan fragments from OnePlan.

```
GET https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/list-workplan-fragments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePlan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/list-workplan-fragments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePlan/latest/actions/list-workplan-fragments?${params}`, {
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
| `FragmentCategory` | string | no | Optional fragment category query parameter from the docs. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnePlan API returns.

## Native endpoint

Through the native OnePlan API, this operation is `GET /workplan/fragments` (base URL `https://my.oneplan.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workplan-fragments.md) for the provider-specific parameters and requirements.

