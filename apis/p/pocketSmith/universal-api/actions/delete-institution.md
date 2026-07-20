# PocketSmith: Delete Institution

Deletes a PocketSmith institution.

```
DELETE https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/delete-institution
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PocketSmith `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/delete-institution?connectionId=$CONNECTION_ID&institutionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "institutionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/delete-institution?${params}`, {
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
| `institutionId` | number | yes | The unique identifier of the PocketSmith institution. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PocketSmith API returns.

## Native endpoint

Through the native PocketSmith API, this operation is `DELETE /institutions/:id` (base URL `https://api.pocketsmith.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-institution.md) for the provider-specific parameters and requirements.

