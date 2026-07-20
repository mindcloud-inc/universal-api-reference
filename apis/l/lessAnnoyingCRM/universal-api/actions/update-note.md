# Less Annoying CRM: Update Note



```
PUT https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/update-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "noteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/update-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "noteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `noteId` | string | yes | The note Id to update. |
| `note` | string | no | Updated plain-text note body. |
| `dateDisplayedInHistory` | date | no | Updated history timestamp for the note. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Less Annoying CRM API returns.

## Native endpoint

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-note.md) for the provider-specific parameters and requirements.

