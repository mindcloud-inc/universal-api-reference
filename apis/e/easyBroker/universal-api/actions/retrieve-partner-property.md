# EasyBroker: Retrieve Partner Property

Retrieves a property linked to your integration in EasyBroker.

```
GET https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/retrieve-partner-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyBroker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/retrieve-partner-property?connectionId=$CONNECTION_ID&propertyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/retrieve-partner-property?${params}`, {
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
| `propertyId` | string | yes | The EasyBroker property public ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EasyBroker API returns.

## Native endpoint

Through the native EasyBroker API, this operation is `GET /integration_partners/properties/:property_id` (base URL `https://api.easybroker.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-partner-property.md) for the provider-specific parameters and requirements.

