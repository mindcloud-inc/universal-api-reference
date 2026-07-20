# Direct Mail Manager: Get Mailing List



```
GET https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/get-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Direct Mail Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/get-mailing-list?connectionId=$CONNECTION_ID&mlg_lst_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mlg_lst_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/get-mailing-list?${params}`, {
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

Through the native Direct Mail Manager API, this operation is `GET /mailing-lists/:mlg_lst_id` (base URL `https://api.directmailmanager.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mailing-list.md) for the provider-specific parameters and requirements.

