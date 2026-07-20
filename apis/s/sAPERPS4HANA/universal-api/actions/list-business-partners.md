# SAP ERP (S/4HANA): List Business Partners

Retrieves business partners from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partners
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partners?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-business-partners?${params}`, {
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
| `top` | number | no | Maximum number of business partners to return for the list request. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessPartner": "string",
      "businessPartnerCategory": "string",
      "businessPartnerFullName": "Ava Chen",
      "businessPartnerGrouping": "string",
      "businessPartnerName": "Ava Chen",
      "businessPartnerUUID": "string",
      "createdByUser": "string",
      "creationDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessPartner` | string | Business partner identifier. |
| `businessPartnerCategory` | string | Business partner category code. |
| `businessPartnerFullName` | string | Full business partner name. |
| `businessPartnerGrouping` | string | Business partner grouping. |
| `businessPartnerName` | string | Business partner display name. |
| `businessPartnerUUID` | string | Business partner UUID. |
| `createdByUser` | string | User who created the business partner. |
| `creationDate` | date | Creation date. |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_BusinessPartner` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-business-partners.md) for the provider-specific parameters and requirements.

