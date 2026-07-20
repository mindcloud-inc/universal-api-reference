# Happy SMS: Delete Messages Batch



```
DELETE https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/delete-messages-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Happy SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/delete-messages-batch?connectionId=$CONNECTION_ID&queryFilter=id%3D%3D999999999" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queryFilter": "id==999999999"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/delete-messages-batch?${params}`, {
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
| `queryFilter` | string | yes | RSQL filter expression selecting messages to delete. Default: `id==999999999`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "queryFilter": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the matching messages were deleted. |
| `queryFilter` | string | Filter used to select deleted messages. |

## Native endpoint

Through the native Happy SMS API, this operation is `DELETE /api/v1/protected/domain/sms/bulk/messages` (base URL `https://www.api.nc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-messages-batch.md) for the provider-specific parameters and requirements.

