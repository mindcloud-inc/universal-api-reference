# Fivetran: Create Destination

Creates a new destination in your Fivetran account.

```
POST https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/create-destination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fivetran `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/create-destination" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "service": "string",
  "timeZoneOffset": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fivetran/latest/actions/create-destination', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "service": "string",
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
| `groupId` | string | yes | The group ID where the destination belongs. |
| `region` | string | no | Data processing location. |
| `service` | string | yes | The destination service type. |
| `timeZoneOffset` | string | yes | The time zone offset used for the Fivetran sync schedule. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `groupId` | string |  |
| `id` | string |  |
| `region` | string |  |
| `service` | string |  |
| `setupStatus` | string |  |

## Native endpoint

Through the native Fivetran API, this operation is `POST /destinations` (base URL `https://api.fivetran.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-destination.md) for the provider-specific parameters and requirements.

