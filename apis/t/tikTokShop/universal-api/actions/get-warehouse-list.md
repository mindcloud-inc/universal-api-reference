# TikTok Shop: Get Warehouse List

This API retrieves all warehouse information associated with the seller. Warehouse information includes name, status, address, and other details.

```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-warehouse-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-warehouse-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-warehouse-list?${params}`, {
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
| `shopCipher` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "addressLine1": "string",
        "city": "string",
        "contactPerson": "string",
        "distict": "string",
        "fullAddress": "string",
        "phoneNumber": "string",
        "postalCode": "string",
        "region": "string",
        "regionCode": "string",
        "state": "string",
        "town": "string"
      },
      "effectStatus": "string",
      "entityId": "string",
      "id": "string",
      "isDefault": true,
      "name": "Ava Chen",
      "subType": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `address.addressLine1` | string |  |
| `address.city` | string |  |
| `address.contactPerson` | string |  |
| `address.distict` | string |  |
| `address.fullAddress` | string |  |
| `address.phoneNumber` | string |  |
| `address.postalCode` | string |  |
| `address.region` | string |  |
| `address.regionCode` | string |  |
| `address.state` | string |  |
| `address.town` | string |  |
| `effectStatus` | string |  |
| `entityId` | string |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `subType` | string |  |
| `type` | string |  |

## Native endpoint

Through the native TikTok Shop API, this operation is `GET logistics/202309/warehouses` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-warehouse-list.md) for the provider-specific parameters and requirements.

