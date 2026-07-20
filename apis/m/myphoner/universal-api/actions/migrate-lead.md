# Myphoner: Migrate Lead

Moves a lead to another list in Myphoner.

```
PUT https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/migrate-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Myphoner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/migrate-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": 1,
  "toListId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/migrate-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": 1,
    "toListId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `giveBackLeads` | boolean | no | When true, release the lead if it is currently claimed. |
| `leadId` | number | yes | The Myphoner lead ID. |
| `toListId` | number | yes | The destination Myphoner list ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Myphoner API returns.

## Native endpoint

Through the native Myphoner API, this operation is `PATCH /leads/:leadId/migrate` (base URL `https://{{credentials.subdomain}}.myphoner.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/migrate-lead.md) for the provider-specific parameters and requirements.

