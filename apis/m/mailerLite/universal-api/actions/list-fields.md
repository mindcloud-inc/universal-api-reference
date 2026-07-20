# MailerLite: List Fields

Retrieves all subscriber fields from MailerLite.

```
GET https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-fields?${params}`, {
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
| `filter.keyword` | string | no | Returns partial matches for the field name. Example: `country`. |
| `filter.type` | string | no | Field type to include. Example: `text`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort` | string | no | Sort by name or type. Prefix with - for descending. Example: `-name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isDefault": true,
      "key": "string",
      "name": "Ava Chen",
      "type": "string",
      "usedInAutomations": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isDefault` | boolean |  |
| `key` | string |  |
| `name` | string |  |
| `type` | string |  |
| `usedInAutomations` | boolean |  |

## Native endpoint

Through the native MailerLite API, this operation is `GET /fields` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

