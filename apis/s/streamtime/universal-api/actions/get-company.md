# Streamtime: Get Company



```
GET https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-company?connectionId=$CONNECTION_ID&companyId=711949" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "711949"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-company?${params}`, {
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
| `companyId` | number | yes | Company ID Example: `711949`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branchId": 1,
      "branchName": "Ava Chen",
      "companyLeadUserId": 1,
      "companyStatus": {},
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "phone1": "string",
      "phone2": "string",
      "rateCardId": 1,
      "taxNumber": "string",
      "websiteAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branchId` | number | Branch ID |
| `branchName` | string | Branch name |
| `companyLeadUserId` | number | Lead user ID |
| `companyStatus` | object | Company status |
| `id` | number | Company ID |
| `name` | string | Company name |
| `notes` | string | Notes |
| `phone1` | string | Primary phone number |
| `phone2` | string | Secondary phone number |
| `rateCardId` | number | Rate card ID |
| `taxNumber` | string | Tax number |
| `websiteAddress` | string | Website URL |

## Native endpoint

Through the native Streamtime API, this operation is `GET /companies/:company_id` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

