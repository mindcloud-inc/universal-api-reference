# EasyBroker: Update Property Integration

Updates a property integration status in EasyBroker.

```
PUT https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/update-property-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyBroker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/update-property-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyId": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/update-property-integration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyId": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `errorMessage` | list<string> | no | Required if status is failed. Error messages explaining why the listing could not be published or updated. |
| `listingUrl` | string | no | Required if status is successful. The listing URL on your website. |
| `propertyId` | string | yes | The EasyBroker property ID related to the listing on your website. |
| `status` | string | yes | The listing status on your website. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EasyBroker API returns.

## Native endpoint

Through the native EasyBroker API, this operation is `PATCH /integration_partners/properties/:property_id/property_integration` (base URL `https://api.easybroker.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-property-integration.md) for the provider-specific parameters and requirements.

