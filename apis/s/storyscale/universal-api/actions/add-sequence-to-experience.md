# Storyscale: Add Sequence To Experience



```
PUT https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/add-sequence-to-experience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyscale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/add-sequence-to-experience" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "sequenceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/add-sequence-to-experience', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "sequenceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Storyscale experience ID. |
| `sequenceId` | string | yes | The sequence to add to the experience. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Updated experience payload returned by Storyscale. |
| `status` | object | Top-level API status object. |

## Native endpoint

Through the native Storyscale API, this operation is `POST /v1/experience/add-sequence/{id}` (base URL `https://prodapi.storyscale.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-sequence-to-experience.md) for the provider-specific parameters and requirements.

