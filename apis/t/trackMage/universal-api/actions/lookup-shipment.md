# TrackMage: Lookup Shipment

Finds a shipment in TrackMage by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/lookup-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/lookup-shipment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/lookup-shipment?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `search` | string | no |  |
| `orderId` | string | no |  |
| `workspaceId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shipments": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shipments` | array<object> |  |

## Native endpoint

Through the native TrackMage API, this operation is `POST /shipments/lookup` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-shipment.md) for the provider-specific parameters and requirements.

