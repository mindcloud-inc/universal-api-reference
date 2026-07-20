# Week Plan: Delete Action



```
DELETE https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/delete-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/delete-action?connectionId=$CONNECTION_ID&actionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/delete-action?${params}`, {
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
| `actionId` | number | yes | The action to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionId": 1,
      "DeletedAt": "string",
      "IsDeleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionId` | number |  |
| `DeletedAt` | string |  |
| `IsDeleted` | boolean |  |

## Native endpoint

Through the native Week Plan API, this operation is `DELETE actions/:actionId` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-action.md) for the provider-specific parameters and requirements.

