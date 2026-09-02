# Jetbuilt: Get Projects



```
GET https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-projects?${params}`, {
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
| `id` | string | no | Project ID |
| `query` | string | no |  |
| `active` | boolean | no | (true/false) returns projects in an active stage when true; otherwise returns projects in non-active stages |
| `stage` | string | no | Filter projects by stage (a single stage name or a comma separated list - param is ignored when active param is present) Accepts multiple values as an array. |
| `min_created_at` | string | no |  |
| `min_updated_at` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "shortDescription": "string",
      "customId": "string",
      "version": "string",
      "priceValidUntil": "2026-05-07T12:00:00.000Z",
      "probability": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "closeDate": "2026-05-07T12:00:00.000Z",
      "budget": true,
      "paidToDate": {
        "cents": 1,
        "currencyIso": "string"
      },
      "stage": "string",
      "contractNumber": "string",
      "requiresEngineering?": true,
      "projectType": "string",
      "paymentSchedule": "string",
      "salesTax": 1,
      "laborTax": 1,
      "totalMargin": 1,
      "equipmentMargin": 1,
      "equipmentTotal": 1,
      "laborTotal": 1,
      "shippingTotal": 1,
      "taxTotal": 1,
      "total": 1,
      "address": "string",
      "city": "Ava Chen",
      "state": "string",
      "zipcode": "string",
      "country": "string",
      "owner": {
        "id": 1,
        "fullName": "Ava Chen"
      },
      "client": {
        "id": 1
      },
      "primaryContact": {
        "id": 1
      },
      "companyLocation": {
        "id": 1,
        "name": "Ava Chen"
      },
      "currency": "string",
      "imageUrl": "https://example.com",
      "active": true,
      "shared": true,
      "originalVersionId": 1,
      "client_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `shortDescription` | string |  |
| `customId` | string |  |
| `version` | string |  |
| `priceValidUntil` | date |  |
| `probability` | number |  |
| `createdAt` | date |  |
| `updatedAt` | date |  |
| `closeDate` | date |  |
| `budget` | boolean |  |
| `paidToDate.cents` | number |  |
| `paidToDate.currencyIso` | string |  |
| `stage` | string |  |
| `contractNumber` | string |  |
| `requiresEngineering?` | boolean |  |
| `projectType` | string |  |
| `paymentSchedule` | string |  |
| `salesTax` | number |  |
| `laborTax` | number |  |
| `totalMargin` | number |  |
| `equipmentMargin` | number |  |
| `equipmentTotal` | number |  |
| `laborTotal` | number |  |
| `shippingTotal` | number |  |
| `taxTotal` | number |  |
| `total` | number |  |
| `address` | string |  |
| `city` | string |  |
| `state` | string |  |
| `zipcode` | string |  |
| `country` | string |  |
| `owner.id` | number |  |
| `owner.fullName` | string |  |
| `client.id` | number |  |
| `primaryContact.id` | number |  |
| `companyLocation.id` | number |  |
| `companyLocation.name` | string |  |
| `currency` | string |  |
| `imageUrl` | string |  |
| `active` | boolean |  |
| `shared` | boolean |  |
| `originalVersionId` | number |  |
| `client_name` | string |  |

## Native endpoint

Through the native Jetbuilt API, this operation is `GET projects/:id` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-projects.md) for the provider-specific parameters and requirements.

