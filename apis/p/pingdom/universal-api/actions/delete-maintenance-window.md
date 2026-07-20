# Pingdom: Delete Maintenance Window



```
DELETE https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/delete-maintenance-window
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/delete-maintenance-window?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/delete-maintenance-window?${params}`, {
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
| `id` | number | yes | Identifier of the maintenance window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Pingdom API, this operation is `DELETE /maintenance/:id` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-maintenance-window.md) for the provider-specific parameters and requirements.

