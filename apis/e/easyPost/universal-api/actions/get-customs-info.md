# EasyPost: Get Customs Info

Retrieves details for customs info from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-customs-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-customs-info?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/get-customs-info?${params}`, {
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
| `id` | string | yes | EasyPost CustomsInfo ID, beginning with cstinfo_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentsType": "string",
      "customsCertify": true,
      "customsItems": [
        {}
      ],
      "customsSigner": "string",
      "eelPfc": "string",
      "id": "string",
      "mode": "string",
      "nonDeliveryOption": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentsType` | string |  |
| `customsCertify` | boolean |  |
| `customsItems` | array<object> |  |
| `customsSigner` | string |  |
| `eelPfc` | string |  |
| `id` | string |  |
| `mode` | string |  |
| `nonDeliveryOption` | string |  |
| `object` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `GET /customs_infos/:id` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customs-info.md) for the provider-specific parameters and requirements.

