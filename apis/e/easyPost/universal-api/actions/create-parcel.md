# EasyPost: Create Parcel

Creates a new parcel in EasyPost.

```
POST https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-parcel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-parcel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parcel": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-parcel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parcel": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parcel` | object | yes | Parcel object to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "height": 1,
      "id": "string",
      "length": 1,
      "mode": "string",
      "object": "string",
      "predefinedPackage": "string",
      "weight": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `height` | number |  |
| `id` | string |  |
| `length` | number |  |
| `mode` | string |  |
| `object` | string |  |
| `predefinedPackage` | string |  |
| `weight` | number |  |
| `width` | number |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /parcels` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-parcel.md) for the provider-specific parameters and requirements.

