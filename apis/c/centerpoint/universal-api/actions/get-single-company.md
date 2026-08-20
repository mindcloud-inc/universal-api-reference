# Centerpoint: Get Company



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-company?connectionId=$CONNECTION_ID&COMPANY_ID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "COMPANY_ID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-company?${params}`, {
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
| `COMPANY_ID` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[companies]` | string | no | Optional fields companies query parameter. |
| `fields[profiles]` | string | no | Optional fields profiles query parameter. |
| `fields[employees]` | string | no | Optional fields employees query parameter. |
| `include` | string | no | Optional include query parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "accountId": 1,
        "closeRate": "string",
        "country": "string",
        "county": "string",
        "createdAt": "string",
        "custom": {
          "licensed": {}
        },
        "customWithLabels": {
          "licensed": {}
        },
        "deletedAt": {},
        "externalId": "string",
        "importId": {},
        "latitude": 1,
        "locality": "string",
        "longitude": 1,
        "name": "Ava Chen",
        "options": {
          "dailyProgressReportIncludedWork": "string",
          "dailyProgressReportTimeOfDay": "string",
          "isHideProductPriceFromTechnicians": true,
          "serviceBillingInstructions": "string",
          "taxLabelOverride": "string"
        },
        "placeId": "string",
        "postalCode": "string",
        "propertyCount": 1,
        "recentActivity": "string",
        "region": "string",
        "salesStatus": "string",
        "streetAddress": "string",
        "subpremise": {},
        "timezone": "string",
        "type": "string",
        "updatedAt": "string",
        "website": {}
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.accountId` | number |  |
| `attributes.closeRate` | string |  |
| `attributes.country` | string |  |
| `attributes.county` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.custom.licensed` | object |  |
| `attributes.customWithLabels.licensed` | object |  |
| `attributes.deletedAt` | object |  |
| `attributes.externalId` | string |  |
| `attributes.importId` | object |  |
| `attributes.latitude` | number |  |
| `attributes.locality` | string |  |
| `attributes.longitude` | number |  |
| `attributes.name` | string |  |
| `attributes.options.dailyProgressReportIncludedWork` | string |  |
| `attributes.options.dailyProgressReportTimeOfDay` | string |  |
| `attributes.options.isHideProductPriceFromTechnicians` | boolean |  |
| `attributes.options.serviceBillingInstructions` | string |  |
| `attributes.options.taxLabelOverride` | string |  |
| `attributes.placeId` | string |  |
| `attributes.postalCode` | string |  |
| `attributes.propertyCount` | number |  |
| `attributes.recentActivity` | string |  |
| `attributes.region` | string |  |
| `attributes.salesStatus` | string |  |
| `attributes.streetAddress` | string |  |
| `attributes.subpremise` | object |  |
| `attributes.timezone` | string |  |
| `attributes.type` | string |  |
| `attributes.updatedAt` | string |  |
| `attributes.website` | object |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET companies/:COMPANY_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-company.md) for the provider-specific parameters and requirements.

