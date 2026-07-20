# Zoho Tables: Update Base

Updates an existing base in Zoho Tables.

```
PUT https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/update-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/update-base" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalId": 1,
  "baseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/update-base', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalId": 1,
    "baseId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalId` | number | yes |  |
| `baseId` | string | yes |  |
| `baseName` | string | no |  |
| `baseIcon` | number | no |  |
| `baseColor` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseId": "string",
      "color": "string",
      "icon": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseId` | string | Zoho base identifier. |
| `color` | string | Base color token. |
| `icon` | number | Base icon code. |
| `name` | string | Base name. |

## Native endpoint

Through the native Zoho Tables API, this operation is `PUT /bases` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-base.md) for the provider-specific parameters and requirements.

