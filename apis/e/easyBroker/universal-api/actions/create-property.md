# EasyBroker: Create Property

Creates a new property in EasyBroker.

```
POST https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/create-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyBroker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/create-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyType": "string",
  "operations[0].type": "string",
  "operations[0].amount": 1,
  "title": "string",
  "description": "string",
  "status": "not_published",
  "street": "string",
  "location.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/create-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyType": "string",
    "operations[0].type": "string",
    "operations[0].amount": 1,
    "title": "string",
    "description": "string",
    "status": "not_published",
    "street": "string",
    "location.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertyType` | string | yes | Property type exactly as registered in EasyBroker. |
| `operations[0].type` | string | yes | Primary operation type, for example sale or rental. |
| `operations[0].amount` | number | yes | Primary operation amount. |
| `title` | string | yes | Property title. |
| `description` | string | yes | Property description. |
| `status` | string | yes | Property status, recommended not_published for initial creation. Default: `not_published`. |
| `street` | string | yes | Property street. |
| `location.name` | string | yes | Location name matching EasyBroker location data. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EasyBroker API returns.

## Native endpoint

Through the native EasyBroker API, this operation is `POST /properties` (base URL `https://api.easybroker.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-property.md) for the provider-specific parameters and requirements.

