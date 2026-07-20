# Beebole: Update a Company

Updates an existing company in Beebole.

```
PUT https://connect.mindcloud.co/v1/universal/beebole/latest/actions/update-a-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beebole `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/beebole/latest/actions/update-a-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "company.id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beebole/latest/actions/update-a-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "company.id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company.id` | number | yes | The Beebole company ID to update. |
| `company.name` | string | no | Updated company name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beebole API returns.

## Native endpoint

Through the native Beebole API, this operation is `POST` (base URL `https://beebole-apps.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-company.md) for the provider-specific parameters and requirements.

