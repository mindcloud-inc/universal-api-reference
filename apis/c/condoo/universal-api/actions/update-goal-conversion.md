# condoo: Update Goal Conversion

Updates an existing goal conversion in condoo.

```
PUT https://connect.mindcloud.co/v1/universal/condoo/latest/actions/update-goal-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/update-goal-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/condoo/latest/actions/update-goal-conversion', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversionId` | number | yes | Required goal conversion ID. |
| `key` | string | no | Documented update field; provider docs may be inconsistent for conversion updates. |
| `name` | string | no | Documented update field; provider docs may be inconsistent for conversion updates. |
| `path` | string | no | Documented update field; provider docs may be inconsistent for conversion updates. |
| `type` | string | no | Documented update field; provider docs may be inconsistent for conversion updates. |
| `websiteId` | number | no | Documented update field; provider docs may be inconsistent for conversion updates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native condoo API, this operation is `POST /goals-conversions/{conversion_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-goal-conversion.md) for the provider-specific parameters and requirements.

