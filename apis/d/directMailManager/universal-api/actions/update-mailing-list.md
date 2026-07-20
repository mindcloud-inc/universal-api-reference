# Direct Mail Manager: Update Mailing List



```
PUT https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/update-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Direct Mail Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/update-mailing-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mlg_lst_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/update-mailing-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mlg_lst_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mlg_lst_id` | string | yes | The unique ID of the mailing list. |
| `name` | string | no | The updated mailing list name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses_count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "locked_at": "2026-05-07T12:00:00.000Z",
      "mailable_count": 1,
      "metadata": [
        {}
      ],
      "name": "Ava Chen",
      "object": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses_count` | number |  |
| `created_at` | date |  |
| `id` | string |  |
| `locked_at` | date |  |
| `mailable_count` | number |  |
| `metadata` | array<object> |  |
| `name` | string |  |
| `object` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Direct Mail Manager API, this operation is `PUT /mailing-lists/:mlg_lst_id` (base URL `https://api.directmailmanager.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-mailing-list.md) for the provider-specific parameters and requirements.

