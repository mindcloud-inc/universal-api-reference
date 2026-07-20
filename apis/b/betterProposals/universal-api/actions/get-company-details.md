# Better Proposals: Get Company Details

Retrieves company details from Better Proposals.

```
GET https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-company-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-company-details?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/get-company-details?${params}`, {
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
| `companyId` | string | yes | The Better Proposals company ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountID": "string",
      "companyCRMID": {},
      "companyName": "Ava Chen",
      "createdBy": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateEdited": "2026-05-07T12:00:00.000Z",
      "deleted": "string",
      "deletedBy": {},
      "demoCompany": "string",
      "editedBy": {},
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountID` | string |  |
| `companyCRMID` | object |  |
| `companyName` | string |  |
| `createdBy` | string |  |
| `dateCreated` | date |  |
| `dateEdited` | date |  |
| `deleted` | string |  |
| `deletedBy` | object |  |
| `demoCompany` | string |  |
| `editedBy` | object |  |
| `id` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `GET /company/:COMPANY_ID` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-details.md) for the provider-specific parameters and requirements.

