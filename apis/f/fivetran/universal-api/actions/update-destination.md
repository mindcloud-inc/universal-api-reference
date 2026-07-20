# Fivetran: Update Destination

Updates an existing destination in your Fivetran account.

```
PUT https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/update-destination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/update-destination" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationId": "string",
  "timeZoneOffset": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/update-destination', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationId": "string",
    "timeZoneOffset": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `config` | object | no | Destination setup configuration object. |
| `destinationId` | string | yes | The unique identifier for the destination within Fivetran. |
| `timeZoneOffset` | string | yes | The time zone offset used for the Fivetran sync schedule. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "groupId": "string",
      "id": "string",
      "region": "string",
      "service": "string",
      "setupStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `groupId` | string |  |
| `id` | string |  |
| `region` | string |  |
| `service` | string |  |
| `setupStatus` | string |  |

## Native endpoint

Through the native Fivetran API, this operation is `PATCH /destinations/[:destinationId]` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-destination.md) for the provider-specific parameters and requirements.

