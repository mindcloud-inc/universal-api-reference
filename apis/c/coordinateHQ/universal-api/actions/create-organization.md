# CoordinateHQ: Create Organization



```
POST https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/create-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoordinateHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/create-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/create-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationName` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entityType": "string",
      "externalObjectId": {},
      "lastModifiedDt": "string",
      "organizationDescription": {},
      "organizationId": "string",
      "organizationName": "Ava Chen",
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entityType` | string |  |
| `externalObjectId` | object |  |
| `lastModifiedDt` | string |  |
| `organizationDescription` | object |  |
| `organizationId` | string |  |
| `organizationName` | string |  |
| `vendorId` | string |  |

## Native endpoint

Through the native CoordinateHQ API, this operation is `POST /organizations` (base URL `https://app.coordinatehq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization.md) for the provider-specific parameters and requirements.

