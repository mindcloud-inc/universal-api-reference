# ServiceTitan: Get Payment Terms

Retrieves payment terms from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-payment-terms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-payment-terms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-payment-terms?${params}`, {
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
      "active": true,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "dueDay": 1,
      "dueDayType": "string",
      "id": 1,
      "inUse": true,
      "isCustomerDefault": true,
      "isVendorDefault": true,
      "modifiedOn": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdOn` | date |  |
| `dueDay` | number |  |
| `dueDayType` | string |  |
| `id` | number |  |
| `inUse` | boolean |  |
| `isCustomerDefault` | boolean |  |
| `isVendorDefault` | boolean |  |
| `modifiedOn` | date |  |
| `name` | string |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET accounting/v2/tenant/{{credentials.tenant}}/payment-terms` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment-terms.md) for the provider-specific parameters and requirements.

