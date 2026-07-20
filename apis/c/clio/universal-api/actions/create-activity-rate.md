# Clio Manage: Create Activity Rate

Creates a new activity rate in Clio Manage.

```
POST https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-activity-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Manage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-activity-rate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.contact_id": 1,
  "data.rate": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clio/latest/actions/create-activity-rate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.contact_id": 1,
    "data.rate": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.contact_id` | number | yes | Contact associated with this activity rate. |
| `data.rate` | number | yes | Hourly or flat monetary rate. |
| `data.flat_rate` | boolean | no | Whether this rate should be treated as a flat rate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": 1,
      "rate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | number |  |
| `rate` | number |  |

## Native endpoint

Through the native Clio Manage API, this operation is `POST /activity_rates.json` (base URL `https://app.clio.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-activity-rate.md) for the provider-specific parameters and requirements.

