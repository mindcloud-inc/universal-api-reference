# Channex: List Channel Availability Rules

Retrieves channel availability rules from Channex.

```
GET https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-channel-availability-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channex `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-channel-availability-rules?connectionId=$CONNECTION_ID&limit=25&offset=0&propertyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "propertyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channex/latest/actions/list-channel-availability-rules?${params}`, {
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
| `propertyId` | string | yes | Property UUID required by the channel availability rules list endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].attributes.end_date` | date |  |
| `data[].attributes.property_id` | string |  |
| `data[].attributes.start_date` | date |  |
| `data[].attributes.type` | string |  |
| `data[].attributes.value` | number |  |
| `data[].id` | string |  |
| `data[].type` | string |  |

## Native endpoint

Through the native Channex API, this operation is `GET /channel_availability_rules` (base URL `https://staging.channex.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channel-availability-rules.md) for the provider-specific parameters and requirements.

