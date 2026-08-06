# Avalara AvaTax: Get Customer



```
GET https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-customer?connectionId=$CONNECTION_ID&companyId=1&customerCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1",
  "customerCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-customer?${params}`, {
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
| `companyId` | number | yes | Avalara company ID. |
| `customerCode` | string | yes | Avalara customer code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "companyId": 1,
      "country": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "customerCode": "string",
      "id": 1,
      "isBill": true,
      "isShip": true,
      "line1": "string",
      "line2": "string",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "postalCode": "string",
      "region": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `companyId` | number |  |
| `country` | string |  |
| `createdDate` | date |  |
| `customerCode` | string |  |
| `id` | number |  |
| `isBill` | boolean |  |
| `isShip` | boolean |  |
| `line1` | string |  |
| `line2` | string |  |
| `modifiedDate` | date |  |
| `name` | string |  |
| `postalCode` | string |  |
| `region` | string |  |

## Native endpoint

Through the native Avalara AvaTax API, this operation is `GET companies/:companyId/customers/:customerCode` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

