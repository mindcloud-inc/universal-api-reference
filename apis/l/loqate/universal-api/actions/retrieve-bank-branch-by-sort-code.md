# Loqate: Retrieve Bank Branch By Sort Code

Retrieves a bank branch from Loqate by sort code.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/retrieve-bank-branch-by-sort-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/retrieve-bank-branch-by-sort-code?connectionId=$CONNECTION_ID&sortCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sortCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/retrieve-bank-branch-by-sort-code?${params}`, {
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
| `sortCode` | string | yes | The branch sort code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bank": "string",
      "bankBIC": "string",
      "branch": "string",
      "branchBIC": "string",
      "cHAPSSupported": true,
      "contactAddressLine1": "string",
      "contactAddressLine2": "string",
      "contactFax": "string",
      "contactPhone": "string",
      "contactPostcode": "string",
      "contactPostTown": "string",
      "fasterPaymentsSupported": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bank` | string |  |
| `bankBIC` | string |  |
| `branch` | string |  |
| `branchBIC` | string |  |
| `cHAPSSupported` | boolean |  |
| `contactAddressLine1` | string |  |
| `contactAddressLine2` | string |  |
| `contactFax` | string |  |
| `contactPhone` | string |  |
| `contactPostcode` | string |  |
| `contactPostTown` | string |  |
| `fasterPaymentsSupported` | boolean |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /BankAccountValidation/Interactive/RetrieveBySortcode/v1.00/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-bank-branch-by-sort-code.md) for the provider-specific parameters and requirements.

