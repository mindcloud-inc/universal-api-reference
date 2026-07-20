# TrueMail: Create Filter

Creates a new blocklist filter in TrueMail.

```
POST https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/create-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrueMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/create-filter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filterType": "0",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/create-filter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filterType": "0",
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterType` | string | yes | The type of filter to create. One of: `0`, `1`, `2`. |
| `value` | string | yes | The email, domain, or IP address to block. |
| `reason` | string | no | Optional reason for the filter entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filter": {
        "createdAt": "string",
        "filterType": "string",
        "id": 1,
        "reason": "string",
        "updatedAt": "string",
        "userId": 1,
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filter.createdAt` | string |  |
| `filter.filterType` | string |  |
| `filter.id` | number |  |
| `filter.reason` | string |  |
| `filter.updatedAt` | string |  |
| `filter.userId` | number |  |
| `filter.value` | string |  |

## Native endpoint

Through the native TrueMail API, this operation is `POST /v1/filters` (base URL `https://api.mailcop.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-filter.md) for the provider-specific parameters and requirements.

