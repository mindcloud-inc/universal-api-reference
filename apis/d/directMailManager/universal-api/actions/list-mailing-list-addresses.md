# Direct Mail Manager: List Mailing List Addresses



```
GET https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/list-mailing-list-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Direct Mail Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/list-mailing-list-addresses?connectionId=$CONNECTION_ID&mlg_lst_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mlg_lst_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/list-mailing-list-addresses?${params}`, {
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
      "address_city": "string",
      "address_country": "string",
      "address_line1": "string",
      "address_line2": "string",
      "address_state": "string",
      "address_zip": "string",
      "company": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "first_name": "Ava",
      "id": "string",
      "is_deliverable": true,
      "last_name": "Chen",
      "object": "string",
      "suppressed_at": "2026-05-07T12:00:00.000Z",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "verification_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_city` | string |  |
| `address_country` | string |  |
| `address_line1` | string |  |
| `address_line2` | string |  |
| `address_state` | string |  |
| `address_zip` | string |  |
| `company` | string |  |
| `created_at` | date |  |
| `first_name` | string |  |
| `id` | string |  |
| `is_deliverable` | boolean |  |
| `last_name` | string |  |
| `object` | string |  |
| `suppressed_at` | date |  |
| `updated_at` | date |  |
| `verification_status` | string |  |

## Native endpoint

Through the native Direct Mail Manager API, this operation is `GET /mailing-lists/:mlg_lst_id/addresses` (base URL `https://api.directmailmanager.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mailing-list-addresses.md) for the provider-specific parameters and requirements.

