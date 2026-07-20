# NetHunt CRM: Create Record

Creates a new record in NetHunt CRM.

```
POST https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetHunt CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fields": {},
  "folderId": "string",
  "timeZone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netHuntCRM/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fields": {},
    "folderId": "string",
    "timeZone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | object | yes | Record fields payload keyed by NetHunt field name. |
| `folderId` | string | yes | Folder ID to create the record in. |
| `timeZone` | string | yes | User time zone used when creating the record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fields": {},
      "link": "https://example.com",
      "recordId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `fields` | object |  |
| `link` | string |  |
| `recordId` | string |  |

## Native endpoint

Through the native NetHunt CRM API, this operation is `POST /actions/create-record/:folderId` (base URL `https://nethunt.com/api/v1/zapier`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record.md) for the provider-specific parameters and requirements.

