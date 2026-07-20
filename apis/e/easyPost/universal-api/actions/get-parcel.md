# EasyPost: Get Parcel

Retrieves details for a parcel from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-parcel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-parcel?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-parcel?${params}`, {
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
| `id` | string | yes | EasyPost Parcel ID, beginning with prcl_. |

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

Through the native EasyPost API, this operation is `GET /parcels/:id` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-parcel.md) for the provider-specific parameters and requirements.

