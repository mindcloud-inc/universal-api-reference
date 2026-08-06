# Avalara AvaTax: Get Tax Code



```
GET https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-tax-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-tax-code?connectionId=$CONNECTION_ID&companyId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-tax-code?${params}`, {
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
| `companyId` | number | yes | The ID of the company that owns this tax code. |
| `id` | number | yes | The numeric ID of the tax code to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "createdUserId": 1,
      "description": "string",
      "goodsServiceCode": 1,
      "id": 1,
      "isActive": true,
      "isPhysical": true,
      "isSSTCertified": true,
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifiedUserId": 1,
      "taxCode": "string",
      "taxCodeTypeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `createdDate` | date |  |
| `createdUserId` | number |  |
| `description` | string |  |
| `goodsServiceCode` | number |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isPhysical` | boolean |  |
| `isSSTCertified` | boolean |  |
| `modifiedDate` | date |  |
| `modifiedUserId` | number |  |
| `taxCode` | string |  |
| `taxCodeTypeId` | string |  |

## Native endpoint

Through the native Avalara AvaTax API, this operation is `GET companies/:companyId/taxcodes/:id` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tax-code.md) for the provider-specific parameters and requirements.

