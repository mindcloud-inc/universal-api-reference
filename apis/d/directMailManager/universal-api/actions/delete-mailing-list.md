# Direct Mail Manager: Delete Mailing List



```
DELETE https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/delete-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Direct Mail Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/delete-mailing-list?connectionId=$CONNECTION_ID&mlg_lst_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mlg_lst_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/delete-mailing-list?${params}`, {
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
| `mlg_lst_id` | string | yes | The unique ID of the mailing list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | string |  |

## Native endpoint

Through the native Direct Mail Manager API, this operation is `DELETE /mailing-lists/:mlg_lst_id` (base URL `https://api.directmailmanager.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-mailing-list.md) for the provider-specific parameters and requirements.

