# Chat Aid: Delete Custom Source

Deletes an existing custom source from Chat Aid.

```
DELETE https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/delete-custom-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chat Aid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/delete-custom-source?connectionId=$CONNECTION_ID&id=65e1c08202791119fbe1d476" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "65e1c08202791119fbe1d476"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/delete-custom-source?${params}`, {
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
| `id` | string | yes | Custom source ID to delete. Example: `65e1c08202791119fbe1d476`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |

## Native endpoint

Through the native Chat Aid API, this operation is `DELETE /external/sources/custom/:id` (base URL `https://api.chataid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-custom-source.md) for the provider-specific parameters and requirements.

