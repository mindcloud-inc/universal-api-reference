# USAC: Get Data



```
GET https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/get-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a USAC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/get-data?connectionId=$CONNECTION_ID&resourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSAC/latest/actions/get-data?${params}`, {
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
| `resourceId` | string | yes | This is the ID of the dataset, use the List Datasets action to retrieve this. |
| `where` | string | no | Used similar to SQL where. Docs: https://dev.socrata.com/docs/queries/where |
| `orderBy` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationNumber": "string",
      "autAddress1": "string",
      "autCity": "string",
      "autEmail": "ava@example.com",
      "autEmployer": "string",
      "autFirstName": "Ava",
      "autLastName": "Chen",
      "autPhone": "string",
      "autState": "string",
      "autTitle": "string",
      "autZipcode": "string",
      "c1Discount": "string",
      "c1VoiceDiscount": "string",
      "c2Discount": "string",
      "certifiedDatetime": "string",
      "chosenCategoryOfService": "string",
      "cnctEmail": "ava@example.com",
      "cnctFirstName": "Ava",
      "cnctLastName": "Chen",
      "cnctPhone": "string",
      "congressionalDistrict": "string",
      "epcOrganizationId": "string",
      "fccRegistrationNumber": "string",
      "form471StatusName": "Ava Chen",
      "formVersion": "string",
      "fullTimeStudents": "string",
      "fundingRequestAmount": "string",
      "fundingYear": "string",
      "hasServiceProviderListed": "string",
      "isCertifiedInWindow": "string",
      "isUrban": "string",
      "lastModifiedTimestamp": "string",
      "latitude": "string",
      "longitude": "string",
      "nickname": "Ava Chen",
      "nonDiscountShare": "string",
      "nslpPercentage": "string",
      "orgAddress1": "string",
      "organizationEntityTypeName": "Ava Chen",
      "organizationName": "Ava Chen",
      "orgCity": "string",
      "orgEmail": "ava@example.com",
      "orgPhone": "string",
      "orgState": "string",
      "orgZipcode": "string",
      "preDiscountEligibleAmount": "string",
      "receivingFundsDirectly": "string",
      "totalEligibleNslpStudents": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationNumber` | string |  |
| `autAddress1` | string |  |
| `autCity` | string |  |
| `autEmail` | string |  |
| `autEmployer` | string |  |
| `autFirstName` | string |  |
| `autLastName` | string |  |
| `autPhone` | string |  |
| `autState` | string |  |
| `autTitle` | string |  |
| `autZipcode` | string |  |
| `c1Discount` | string |  |
| `c1VoiceDiscount` | string |  |
| `c2Discount` | string |  |
| `certifiedDatetime` | string |  |
| `chosenCategoryOfService` | string |  |
| `cnctEmail` | string |  |
| `cnctFirstName` | string |  |
| `cnctLastName` | string |  |
| `cnctPhone` | string |  |
| `congressionalDistrict` | string |  |
| `epcOrganizationId` | string |  |
| `fccRegistrationNumber` | string |  |
| `form471StatusName` | string |  |
| `formVersion` | string |  |
| `fullTimeStudents` | string |  |
| `fundingRequestAmount` | string |  |
| `fundingYear` | string |  |
| `hasServiceProviderListed` | string |  |
| `isCertifiedInWindow` | string |  |
| `isUrban` | string |  |
| `lastModifiedTimestamp` | string |  |
| `latitude` | string |  |
| `longitude` | string |  |
| `nickname` | string |  |
| `nonDiscountShare` | string |  |
| `nslpPercentage` | string |  |
| `orgAddress1` | string |  |
| `organizationEntityTypeName` | string |  |
| `organizationName` | string |  |
| `orgCity` | string |  |
| `orgEmail` | string |  |
| `orgPhone` | string |  |
| `orgState` | string |  |
| `orgZipcode` | string |  |
| `preDiscountEligibleAmount` | string |  |
| `receivingFundsDirectly` | string |  |
| `totalEligibleNslpStudents` | string |  |

## Native endpoint

Through the native USAC API, this operation is `GET resource/:resourceId.json` (base URL `https://opendata.usac.org/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data.md) for the provider-specific parameters and requirements.

