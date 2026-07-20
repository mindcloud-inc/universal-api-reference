# Listclean: Delete List

Deletes a verification list from Listclean.

```
DELETE https://connect.mindcloud.co/v1/universal/listclean/latest/actions/delete-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/delete-list?connectionId=$CONNECTION_ID&list_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/listclean/latest/actions/delete-list?${params}`, {
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
| `list_id` | number | yes | List ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error_code": 1,
      "message": "string",
      "success": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error_code` | number | Provider error code. |
| `message` | string | Delete result message. |
| `success` | number | Provider success flag. |

## Native endpoint

Through the native Listclean API, this operation is `DELETE /lists/:list_id` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-list.md) for the provider-specific parameters and requirements.

