# Zoho FSM: List Work Orders

Retrieves work orders from Zoho FSM.

```
GET https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-work-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-work-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-work-orders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "$currencySymbol": "string",
      "$editable": true,
      "$inactive": true,
      "$permissions": {
        "delete": true,
        "edit": true,
        "read": true
      },
      "adjustment": 1,
      "billingAddress": {
        "billingCity": "string",
        "billingCountry": "string",
        "billingState": "string",
        "billingStreet1": "string",
        "billingZipCode": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "billingStatus": "string",
      "company": {
        "id": "string",
        "name": "Ava Chen"
      },
      "config": "string",
      "contact": {
        "id": "string",
        "name": "Ava Chen"
      },
      "createdBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "discountType": "string",
      "exchangeRate": 1,
      "grandTotal": 1,
      "id": "string",
      "location": "string",
      "modifiedBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "owner": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "roundOff": 1,
      "serviceAddress": {
        "id": "string",
        "name": "Ava Chen",
        "serviceCity": "string",
        "serviceCountry": "string",
        "serviceState": "string",
        "serviceStreet1": "string",
        "serviceZipCode": "string"
      },
      "status": "string",
      "subTotal": 1,
      "summary": "string",
      "taxAmount": 1,
      "territory": {
        "id": "string",
        "name": "Ava Chen"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$currencySymbol` | string |  |
| `$editable` | boolean |  |
| `$inactive` | boolean |  |
| `$permissions.delete` | boolean |  |
| `$permissions.edit` | boolean |  |
| `$permissions.read` | boolean |  |
| `adjustment` | number |  |
| `billingAddress.billingCity` | string |  |
| `billingAddress.billingCountry` | string |  |
| `billingAddress.billingState` | string |  |
| `billingAddress.billingStreet1` | string |  |
| `billingAddress.billingZipCode` | string |  |
| `billingAddress.id` | string |  |
| `billingAddress.name` | string |  |
| `billingStatus` | string |  |
| `company.id` | string |  |
| `company.name` | string |  |
| `config` | string |  |
| `contact.id` | string |  |
| `contact.name` | string |  |
| `createdBy.email` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdTime` | date |  |
| `currency` | string |  |
| `discountType` | string |  |
| `exchangeRate` | number |  |
| `grandTotal` | number |  |
| `id` | string |  |
| `location` | string |  |
| `modifiedBy.email` | string |  |
| `modifiedBy.id` | string |  |
| `modifiedBy.name` | string |  |
| `modifiedTime` | date |  |
| `name` | string |  |
| `owner.email` | string |  |
| `owner.id` | string |  |
| `owner.name` | string |  |
| `roundOff` | number |  |
| `serviceAddress.id` | string |  |
| `serviceAddress.name` | string |  |
| `serviceAddress.serviceCity` | string |  |
| `serviceAddress.serviceCountry` | string |  |
| `serviceAddress.serviceState` | string |  |
| `serviceAddress.serviceStreet1` | string |  |
| `serviceAddress.serviceZipCode` | string |  |
| `status` | string |  |
| `subTotal` | number |  |
| `summary` | string |  |
| `taxAmount` | number |  |
| `territory.id` | string |  |
| `territory.name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `GET /Work_Orders` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-work-orders.md) for the provider-specific parameters and requirements.

