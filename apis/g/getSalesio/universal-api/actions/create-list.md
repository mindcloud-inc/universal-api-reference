# GetSales.io: Create List



```
POST https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetSales.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "CMO Germany"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/getSalesio/latest/actions/create-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "CMO Germany"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the new list. Example: `CMO Germany`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "team_id": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `team_id` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native GetSales.io API, this operation is `POST /leads/api/lists` (base URL `https://amazing.getsales.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

