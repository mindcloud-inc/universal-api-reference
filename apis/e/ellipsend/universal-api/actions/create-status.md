# Ellipsend: Create Status

Creates a new status in Ellipsend.

```
POST https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/create-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ellipsend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/create-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ellipsend/latest/actions/create-status', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | yes | The status name to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Ellipsend API, this operation is `POST /status` (base URL `https://api.ellipsend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-status.md) for the provider-specific parameters and requirements.

