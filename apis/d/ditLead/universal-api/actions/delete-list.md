# DitLead: Delete List



```
DELETE https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/delete-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/delete-list?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/delete-list?${params}`, {
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
| `listId` | string | yes | Public ID of the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "deletedList": {
          "listName": "Ava Chen",
          "publicId": "string"
        },
        "message": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.deletedList.listName` | string |  |
| `data.deletedList.publicId` | string |  |
| `data.message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native DitLead API, this operation is `DELETE /v1/list/{listId}` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-list.md) for the provider-specific parameters and requirements.

