# MailerLite: Import Bulk Subscribers to Group

Imports multiple subscribers into a group in MailerLite.

```
PUT https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/import-bulk-subscribers-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/import-bulk-subscribers-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group_id": "180900000000000001",
  "subscribers[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/import-bulk-subscribers-to-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group_id": "180900000000000001",
    "subscribers[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `group_id` | string | yes | Existing MailerLite group identifier. Example: `180900000000000001`. |
| `subscribers[]` | array<object> | yes | Array of subscriber objects to import into the group. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "importProgressUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `importProgressUrl` | string |  |

## Native endpoint

Through the native MailerLite API, this operation is `POST /groups/:group_id/import-subscribers` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-bulk-subscribers-to-group.md) for the provider-specific parameters and requirements.

