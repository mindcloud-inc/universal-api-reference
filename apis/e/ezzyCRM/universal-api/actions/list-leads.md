# EzzyCRM: List Leads



```
GET https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EzzyCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/list-leads?connectionId=$CONNECTION_ID&pipelineId=1&userId=1&fromDate=03%2F01%2F2026&toDate=03%2F31%2F2026" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineId": "1",
  "userId": "1",
  "fromDate": "03/01/2026",
  "toDate": "03/31/2026"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/list-leads?${params}`, {
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
| `pipelineId` | number | yes | Only leads within the given pipeline will be returned. |
| `userId` | number | yes | Live testing showed this value must be supplied for the endpoint to resolve, even though the provider docs describe it as optional. |
| `fromDate` | string | yes | Only leads within the given date range will be returned. Example: `03/01/2026`. |
| `toDate` | string | yes | Only leads within the given date range will be returned. Example: `03/31/2026`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address1": "string",
      "address2": "string",
      "city": "string",
      "contactRemark": "string",
      "country": "string",
      "createdOn": "string",
      "currency": "string",
      "customeField": [
        {
          "fieldName": "Ava Chen",
          "value": "string"
        }
      ],
      "dealId": "string",
      "dealTtile": "string",
      "dealValue": "string",
      "emailAddress": "ava@example.com",
      "expectedCloseDate": "string",
      "firstName": "Ava",
      "industry": "string",
      "jobTitle": "string",
      "lastName": "Chen",
      "leadSource": "string",
      "leadStatus": "string",
      "note": [
        "string"
      ],
      "organization": "string",
      "phone": "string",
      "phoneType": "string",
      "pipeLineName": "Ava Chen",
      "stageName": "Ava Chen",
      "state": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `address2` | string |  |
| `city` | string |  |
| `contactRemark` | string |  |
| `country` | string |  |
| `createdOn` | string |  |
| `currency` | string |  |
| `customeField` | array<object> |  |
| `customeField[].fieldName` | string |  |
| `customeField[].value` | string |  |
| `dealId` | string |  |
| `dealTtile` | string |  |
| `dealValue` | string |  |
| `emailAddress` | string |  |
| `expectedCloseDate` | string |  |
| `firstName` | string |  |
| `industry` | string |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `leadSource` | string |  |
| `leadStatus` | string |  |
| `note` | array<string> |  |
| `organization` | string |  |
| `phone` | string |  |
| `phoneType` | string |  |
| `pipeLineName` | string |  |
| `stageName` | string |  |
| `state` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native EzzyCRM API, this operation is `GET /api/getallleads` (base URL `https://ezzycrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

