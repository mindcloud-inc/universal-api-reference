# Laposta: Delete List

Deletes an existing list from Laposta.

```
DELETE https://connect.mindcloud.co/v1/universal/laposta/latest/actions/delete-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Laposta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/laposta/latest/actions/delete-list?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laposta/latest/actions/delete-list?${params}`, {
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
| `listId` | string | yes | The ID of the list to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "list": {
        "listId": "string",
        "locked": true,
        "name": "Ava Chen",
        "remarks": "string",
        "state": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `list` | object |  |
| `list.listId` | string |  |
| `list.locked` | boolean |  |
| `list.name` | string |  |
| `list.remarks` | string |  |
| `list.state` | string |  |

## Native endpoint

Through the native Laposta API, this operation is `DELETE /list/:listId` (base URL `https://api.laposta.nl/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-list.md) for the provider-specific parameters and requirements.

