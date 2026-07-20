# Channex: Update Channel Availability Rule

Updates a channel availability rule in Channex.

```
PUT https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-channel-availability-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-channel-availability-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "channelAvailabilityRule": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channex/latest/actions/update-channel-availability-rule', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "channelAvailabilityRule": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | UUID of the channel availability rule to update. |
| `channelAvailabilityRule` | object | yes | Top-level channel_availability_rule payload object documented by Channex for rule updates. |

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

Through the native Channex API, this operation is `PUT /channel_availability_rules/:id` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-channel-availability-rule.md) for the provider-specific parameters and requirements.

