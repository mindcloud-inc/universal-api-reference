# Channex: Get Channel Availability Rule

Retrieves a channel availability rule from Channex.

```
GET https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-channel-availability-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-channel-availability-rule?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/get-channel-availability-rule?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | UUID of the channel availability rule to retrieve. |

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

Through the native Channex API, this operation is `GET /channel_availability_rules/:id` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel-availability-rule.md) for the provider-specific parameters and requirements.

