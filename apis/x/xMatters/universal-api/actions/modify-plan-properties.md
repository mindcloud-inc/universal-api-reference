# xMatters: Modify plan properties

Updates plan properties in your xMatters instance.

```
PUT https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-plan-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-plan-properties" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/modify-plan-properties', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `planId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "default": "string",
      "description": "string",
      "helpText": "string",
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "maxLength": 1,
      "minLength": 1,
      "name": "Ava Chen",
      "pattern": "string",
      "propertyType": "string",
      "validate": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default` | string |  |
| `description` | string |  |
| `helpText` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `maxLength` | number |  |
| `minLength` | number |  |
| `name` | string |  |
| `pattern` | string |  |
| `propertyType` | string |  |
| `validate` | boolean |  |

## Native endpoint

Through the native xMatters API, this operation is `POST plans/{planId}/property-definitions` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-plan-properties.md) for the provider-specific parameters and requirements.

