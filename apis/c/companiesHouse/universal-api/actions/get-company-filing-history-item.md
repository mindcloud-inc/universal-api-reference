# Companies House: Get Company Filing History Item

Retrieves a company filing history item from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-filing-history-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-filing-history-item?connectionId=$CONNECTION_ID&companyNumber=string&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyNumber": "string",
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-filing-history-item?${params}`, {
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
| `companyNumber` | string | yes | The company number. |
| `transactionId` | string | yes | The filing transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotations": [
        "string"
      ],
      "barcode": "string",
      "category": "string",
      "date": "string",
      "description": "string",
      "links": {},
      "pages": 1,
      "paper_filed": true,
      "transaction_id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotations` | array |  |
| `barcode` | string |  |
| `category` | string |  |
| `date` | string |  |
| `description` | string |  |
| `links` | object |  |
| `pages` | number |  |
| `paper_filed` | boolean |  |
| `transaction_id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /company/:company_number/filing-history/:transaction_id` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-filing-history-item.md) for the provider-specific parameters and requirements.

