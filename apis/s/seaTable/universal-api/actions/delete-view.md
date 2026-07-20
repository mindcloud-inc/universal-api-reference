# SeaTable: Delete View

Deletes a view from a SeaTable base.

```
DELETE https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/delete-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/delete-view?connectionId=$CONNECTION_ID&viewName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/delete-view?${params}`, {
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
| `viewName` | string | yes | The SeaTable view name. |

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

Through the native SeaTable API, this operation is `DELETE /api-gateway/api/v2/dtables/:base_uuid/views/:view_name/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-view.md) for the provider-specific parameters and requirements.

