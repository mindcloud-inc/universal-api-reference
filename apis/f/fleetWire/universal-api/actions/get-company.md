# FleetWire: Get Company

Retrieves company details from FleetWire.

```
GET https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FleetWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-company?connectionId=$CONNECTION_ID&company=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-company?${params}`, {
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
| `company` | string | yes | The FleetWire company UUID to fetch. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include` | string | no | Comma-separated related resources to include, such as deliveryLocations,taxCategories,listings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object | FleetWire company payload for the authenticated tenant. |

## Native endpoint

Through the native FleetWire API, this operation is `GET /api/v2/company/:company` (base URL `https://api.fleetwire.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

