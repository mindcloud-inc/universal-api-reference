# Leave Dates: Delete Employment

Deletes an existing employment from Leave Dates.

```
DELETE https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/delete-employment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leave Dates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/delete-employment?connectionId=$CONNECTION_ID&id=string&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/delete-employment?${params}`, {
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
| `id` | string | yes | Employment ID |
| `companyId` | string | yes | Company ID for the employment |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leave Dates API returns.

## Native endpoint

Through the native Leave Dates API, this operation is `DELETE /employments/:id` (base URL `https://api.leavedates.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-employment.md) for the provider-specific parameters and requirements.

