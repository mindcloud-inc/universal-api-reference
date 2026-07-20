# Codemagic: Bulk Import Tester Group Contacts

Bulk imports contacts into a Codemagic tester group.

```
POST https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/bulk-import-tester-group-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/bulk-import-tester-group-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "testerGroupId": "string",
  "emails[]": [
    "ava@example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/bulk-import-tester-group-contacts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "testerGroupId": "string",
    "emails[]": ["ava@example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `testerGroupId` | string | yes | Codemagic tester group identifier. |
| `emails[]` | array<string> | yes | Tester contact email addresses to import. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Codemagic API returns.

## Native endpoint

Through the native Codemagic API, this operation is `POST /api/v3/tester-groups/:tester_group_id/contacts` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-import-tester-group-contacts.md) for the provider-specific parameters and requirements.

