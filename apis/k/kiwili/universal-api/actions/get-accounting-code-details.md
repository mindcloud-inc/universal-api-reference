# Kiwili: Get Accounting Code Details

Retrieves details for an accounting code in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-accounting-code-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-accounting-code-details?connectionId=$CONNECTION_ID&accounting_code_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accounting_code_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-accounting-code-details?${params}`, {
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
| `accounting_code_id` | string | yes | The Kiwili accounting code ID. Use the string 0 for the default record when needed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AccountingClass": "string",
      "Code": 1,
      "Description": "string",
      "Id": 1,
      "PercentageTaxReclaim": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountingClass` | string |  |
| `Code` | number |  |
| `Description` | string |  |
| `Id` | number |  |
| `PercentageTaxReclaim` | number |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /accountingcode/:accounting_code_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-accounting-code-details.md) for the provider-specific parameters and requirements.

