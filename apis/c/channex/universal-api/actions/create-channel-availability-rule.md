# Channex: Create Channel Availability Rule

Creates a channel availability rule in Channex.

```
POST https://connect.mindcloud.co/v1/universal/channex/latest/actions/create-channel-availability-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/channex/latest/actions/create-channel-availability-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelAvailabilityRule": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channex/latest/actions/create-channel-availability-rule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelAvailabilityRule": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelAvailabilityRule` | object | yes | Top-level channel_availability_rule payload object documented by Channex for rule creation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "end_date": "2026-05-07T12:00:00.000Z",
          "property_id": "string",
          "start_date": "2026-05-07T12:00:00.000Z",
          "type": "string",
          "value": 1
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.end_date` | date |  |
| `data.attributes.property_id` | string |  |
| `data.attributes.start_date` | date |  |
| `data.attributes.type` | string |  |
| `data.attributes.value` | number |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native Channex API, this operation is `POST /channel_availability_rules` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-channel-availability-rule.md) for the provider-specific parameters and requirements.

