# xMatters: Create plan properties

Creates plan properties in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-plan-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-plan-properties" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/create-plan-properties', {
  method: 'POST',
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
| `default` | string | no |  |
| `description` | string | no |  |
| `helpText` | string | no |  |
| `maxLength` | number | no |  |
| `minLength` | number | no |  |
| `name` | string | no |  |
| `pattern` | string | no |  |
| `planId` | string | no |  |
| `propertyType` | string | no |  |
| `validate` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "default": "2026-05-07T12:00:00.000Z",
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
| `default` | date |  |
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

Through the native xMatters API, this operation is `POST plans/{planId}/property-definitions` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-plan-properties.md) for the provider-specific parameters and requirements.

