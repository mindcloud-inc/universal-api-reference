# Walmart: Bulk Item Enrollment for Walmart+

Manage item participation in the Walmart+ program.

```
PUT https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-item-enrollment-for-walmart-plus
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-item-enrollment-for-walmart-plus" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/walmart/latest/actions/bulk-item-enrollment-for-walmart-plus', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedType` | list<string> | no | Allowed: `PROGRAM_ACTIONS` Default: `PROGRAM_ACTIONS`. |
| `fileName` | file | no |  |
| `requestType` | string | no | `WALMART_PLUS_SFF` - Specifies the type of request for the Walmart+ SFF (Seller-Fulfilled) program. Default: `WALMART_PLUS_SFF`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "feedId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `feedId` | string | A unique identifier, which is returned by the Bulk Upload API, used to track and manage the status of the feed file. |

## Native endpoint

Through the native Walmart API, this operation is `POST /v3/feeds` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-item-enrollment-for-walmart-plus.md) for the provider-specific parameters and requirements.

