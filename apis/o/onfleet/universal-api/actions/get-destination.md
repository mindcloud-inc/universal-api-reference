# Onfleet: Get Destination

Retrieves a destination from Onfleet.

```
GET https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-destination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-destination?connectionId=$CONNECTION_ID&destinationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "destinationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-destination?${params}`, {
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
| `destinationId` | string | yes | The Onfleet destination ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "id": "string",
      "location": [
        1
      ],
      "notes": "string",
      "useGPS": true,
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `id` | string |  |
| `location` | array<number> |  |
| `notes` | string |  |
| `useGPS` | boolean |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native Onfleet API, this operation is `GET /destinations/:destinationId` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-destination.md) for the provider-specific parameters and requirements.

