# Global Patron: Create Datalist Entry Items

Adds datalist entry items to Global Patron.

```
POST https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/create-datalist-entry-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/create-datalist-entry-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "datalistId": "string",
  "entryItems[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/create-datalist-entry-items', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "datalistId": "string",
    "entryItems[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datalistId` | string | yes | ID of the datalist. |
| `entryItems[]` | array<object> | yes | Array of datalist entry items to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created datalist entry item identifier. |

## Native endpoint

Through the native Global Patron API, this operation is `POST /api/restricted/datalist/{datalistId}/entry` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-datalist-entry-items.md) for the provider-specific parameters and requirements.

