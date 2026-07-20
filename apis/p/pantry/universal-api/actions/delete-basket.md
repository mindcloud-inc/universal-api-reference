# Pantry: Delete Basket

Deletes an existing basket from Pantry.

```
DELETE https://connect.mindcloud.co/v1/universal/pantry/latest/actions/delete-basket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pantry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pantry/latest/actions/delete-basket?connectionId=$CONNECTION_ID&basketName=ProjectSettings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "basketName": "ProjectSettings"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pantry/latest/actions/delete-basket?${params}`, {
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
| `basketName` | string | yes | Name of the basket to delete. Example: `ProjectSettings`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pantry API returns.

## Native endpoint

Through the native Pantry API, this operation is `DELETE /pantry/:pantryId/basket/:basketName` (base URL `https://getpantry.cloud/apiv1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-basket.md) for the provider-specific parameters and requirements.

