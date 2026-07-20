# Happy SMS: Delete Message



```
DELETE https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/delete-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Happy SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/delete-message?connectionId=$CONNECTION_ID&id=999999999" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "999999999"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happySMS/latest/actions/delete-message?${params}`, {
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
| `id` | number | yes | Unique SMS identifier. Default: `999999999`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the SMS was deleted. |
| `id` | number | Identifier of the deleted SMS. |

## Native endpoint

Through the native Happy SMS API, this operation is `DELETE /api/v1/protected/domain/sms/messages/:id` (base URL `https://www.api.nc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message.md) for the provider-specific parameters and requirements.

