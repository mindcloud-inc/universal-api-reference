# TrueMail: Delete Filter

Deletes an existing blocklist filter from TrueMail.

```
DELETE https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/delete-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/delete-filter?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/delete-filter?${params}`, {
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
| `id` | string | yes | The filter identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TrueMail API, this operation is `DELETE /v1/filters/{{id}}` (base URL `https://api.mailcop.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-filter.md) for the provider-specific parameters and requirements.

