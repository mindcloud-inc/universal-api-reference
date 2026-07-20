# Hey Reach: Add Leads To List

Adds leads to a list in Hey Reach.

```
PUT https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/add-leads-to-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/add-leads-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leads[]": [
    {}
  ],
  "listId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/add-leads-to-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leads[]": [{}],
    "listId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leads[]` | array<object> | yes |  |
| `listId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedLeadsCount": 1,
      "failedLeadsCount": 1,
      "updatedLeadsCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedLeadsCount` | number |  |
| `failedLeadsCount` | number |  |
| `updatedLeadsCount` | number |  |

## Native endpoint

Through the native Hey Reach API, this operation is `POST /api/public/list/AddLeadsToListV2` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-leads-to-list.md) for the provider-specific parameters and requirements.

