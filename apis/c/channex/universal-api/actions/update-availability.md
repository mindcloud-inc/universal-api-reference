# Channex: Update Availability

Updates room type availability in Channex.

```
PUT https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-availability" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "values[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-availability', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "values[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `values[]` | array<object> | yes | Array of availability update objects documented by Channex. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "id": "string",
          "type": "string"
        }
      ],
      "meta": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].id` | string |  |
| `data[].type` | string |  |
| `meta.message` | string |  |

## Native endpoint

Through the native Channex API, this operation is `POST /availability` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-availability.md) for the provider-specific parameters and requirements.

