# Jetbuilt: Get Purchasing Sources



```
GET https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-purchasing-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-purchasing-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-purchasing-sources?${params}`, {
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
| `min_updated_at` | string | no |  |
| `project_id` | string | no |  |
| `min_created_at` | string | no |  |
| `iD` | string | no | The ID of the purchasing source to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customId": "string",
      "defaultShip": "string",
      "id": 1,
      "notes": "string",
      "projectId": 1,
      "purchasingSourceId": 1,
      "shipAddress": {
        "city": "Ava Chen",
        "country": "string",
        "postalCode": "string",
        "region": "string",
        "street": "string"
      },
      "shipName": "Ava Chen",
      "shippingOption": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `customId` | string |  |
| `defaultShip` | string |  |
| `id` | number |  |
| `notes` | string |  |
| `projectId` | number |  |
| `purchasingSourceId` | number |  |
| `shipAddress.city` | string |  |
| `shipAddress.country` | string |  |
| `shipAddress.postalCode` | string |  |
| `shipAddress.region` | string |  |
| `shipAddress.street` | string |  |
| `shipName` | string |  |
| `shippingOption` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Jetbuilt API, this operation is `GET purchasing/sources/:iD` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchasing-sources.md) for the provider-specific parameters and requirements.

