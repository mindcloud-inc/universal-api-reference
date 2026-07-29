# Rillion Prime Web Service: List Company Data

List configuration data for one company in Rillion Prime.

```
GET https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-company-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-company-data?connectionId=$CONNECTION_ID&company=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/list-company-data?${params}`, {
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
| `company` | list<string> | yes | Company ID to read. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allocationSetting": "string",
      "arrivalType": "string",
      "baseCurrency": "string",
      "calculateVATAmountOnCostRow": "string",
      "company": "string",
      "erp": "string",
      "invoiceSeries": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocationSetting` | string |  |
| `arrivalType` | string |  |
| `baseCurrency` | string | Accounting currency code. |
| `calculateVATAmountOnCostRow` | string |  |
| `company` | string | Company ID. |
| `erp` | string | ERP identifier configured for the company. |
| `invoiceSeries` | string | Invoice series used by the company. |
| `name` | string | Company name. |

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-data.md) for the provider-specific parameters and requirements.

