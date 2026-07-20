# PocketSmith: Update Institution

Updates a PocketSmith institution.

```
PUT https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/update-institution
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PocketSmith `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/update-institution" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "institutionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pocketSmith/latest/actions/update-institution', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "institutionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currencyCode` | string | no | A new currency code for the institution. |
| `institutionId` | number | yes | The unique identifier of the PocketSmith institution. |
| `title` | string | no | A new title for the institution. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PocketSmith API returns.

## Native endpoint

Through the native PocketSmith API, this operation is `PUT /institutions/:id` (base URL `https://api.pocketsmith.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-institution.md) for the provider-specific parameters and requirements.

