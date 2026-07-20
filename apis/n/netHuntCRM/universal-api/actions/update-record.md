# NetHunt CRM: Update Record

Updates an existing record in NetHunt CRM.

```
PUT https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetHunt CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fieldActions": {},
  "recordId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/update-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fieldActions": {},
    "recordId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldActions` | object | yes | Field actions payload keyed by NetHunt field name, with add/remove/overwrite instructions. |
| `overwrite` | boolean | no | Default overwrite setting for field actions. Default: `false`. |
| `recordId` | string | yes | Record ID to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native NetHunt CRM API, this operation is `POST /actions/update-record/:recordId` (base URL `https://nethunt.com/api/v1/zapier`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-record.md) for the provider-specific parameters and requirements.

