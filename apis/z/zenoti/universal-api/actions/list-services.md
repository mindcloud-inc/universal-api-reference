# Zenoti: List Services



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-services?connectionId=$CONNECTION_ID&centerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "centerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-services?${params}`, {
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
| `centerId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalInfo": "string",
      "addOnsInfo": "string",
      "catalogInfo": "string",
      "code": "string",
      "description": "string",
      "duration": 1,
      "finishingServicesInfo": "string",
      "id": "string",
      "imagePaths": "string",
      "isCoupleService": true,
      "name": "Ava Chen",
      "parallelGroups": "string",
      "parallelServiceGroups": "string",
      "prerequisitesInfo": "string",
      "priceInfo": {
        "currencyId": 1,
        "demandGroupId": "string",
        "includeTax": true,
        "memberPrice": 1,
        "salePrice": 1,
        "ssg": "string",
        "taxId": "string"
      },
      "recoveryTime": 1,
      "variantsInfo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalInfo` | string |  |
| `addOnsInfo` | string |  |
| `catalogInfo` | string |  |
| `code` | string |  |
| `description` | string |  |
| `duration` | number |  |
| `finishingServicesInfo` | string |  |
| `id` | string |  |
| `imagePaths` | string |  |
| `isCoupleService` | boolean |  |
| `name` | string |  |
| `parallelGroups` | string |  |
| `parallelServiceGroups` | string |  |
| `prerequisitesInfo` | string |  |
| `priceInfo.currencyId` | number |  |
| `priceInfo.demandGroupId` | string |  |
| `priceInfo.includeTax` | boolean |  |
| `priceInfo.memberPrice` | number |  |
| `priceInfo.salePrice` | number |  |
| `priceInfo.ssg` | string |  |
| `priceInfo.taxId` | string |  |
| `recoveryTime` | number |  |
| `variantsInfo` | string |  |

## Native endpoint

Through the native Zenoti API, this operation is `GET Centers/:centerId/services` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

