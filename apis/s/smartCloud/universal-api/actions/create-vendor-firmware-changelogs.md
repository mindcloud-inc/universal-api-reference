# 2Smart Cloud: Create firmware changelog



```
POST https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-firmware-changelogs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-firmware-changelogs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "product_version_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/create-vendor-firmware-changelogs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "product_version_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of firmware |
| `changelog` | string | no | Changelog text of firmware |
| `product_version_id` | number | yes | ID of product version |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changelog": "string",
      "created": "string",
      "id": 1,
      "name": "Ava Chen",
      "product_id": 1,
      "product_version_id": 1,
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changelog` | string |  |
| `created` | string |  |
| `id` | number |  |
| `name` | string |  |
| `product_id` | number |  |
| `product_version_id` | number |  |
| `updated` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `POST /vendor/firmware-changelogs` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor-firmware-changelogs.md) for the provider-specific parameters and requirements.

