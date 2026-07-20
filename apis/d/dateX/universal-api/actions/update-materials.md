# DateX (Legacy): Update Materials



```
PUT https://connect.mindcloud.co/v1/universal/dateX/latest/actions/update-materials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX (Legacy) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dateX/latest/actions/update-materials" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dateX/latest/actions/update-materials', {
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
| `materials[]` | array | no |  |
| `materials[].packagings[]` | array | no |  |
| `materials[].packagings[].packaging` | string | no | Eg: "EA" |
| `materials[].material_id` | number | no |  |
| `materials[].packagings[].length` | number | no |  |
| `materials[].packagings[].width` | number | no |  |
| `materials[].packagings[].height` | number | no |  |
| `materials[].packagings[].dimension_uom` | string | no | Eg: "ft" |
| `materials[].packagings[].net_weight` | number | no | Eg: 'kg', 'lb' |
| `materials[].packagings[].gross_weight` | number | no |  |
| `materials[].packagings[].weight_uom` | string | no | eg: 'kg', 'lb' |
| `materials[].packagings[].net_volume` | number | no |  |
| `materials[].packagings[].volume_uom` | string | no | eg: 'cu. ft.' |
| `materials[].packagings[].gross_volume` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DateX (Legacy) API returns.

## Native endpoint

Through the native DateX (Legacy) API, this operation is `POST materials/update` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-materials.md) for the provider-specific parameters and requirements.

