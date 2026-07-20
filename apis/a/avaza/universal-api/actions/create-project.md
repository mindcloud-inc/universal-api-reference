# Avaza: Create Project

Creates a new project in Avaza.

```
POST https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projecttitle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projecttitle": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyidfk` | number | no | An ID of a company in Avaza to create the Project under. You must provide either a CompanyID, or a CompanyName |
| `companyname` | string | no | The name for a Company to create the project under. Will create company unless it matches an existing company name |
| `currencycode` | string | no | The ISO 3 letter currency code to use when creating a new Company. If not provided, the account's default currency will be used. |
| `projecttitle` | string | yes | The title of the new project. (255 characters max) |
| `projectcode` | string | no | Used when Manual Project Codes are enabled |
| `projectnotes` | string | no | Any descriptive notes about the project. (2000 characters max) |
| `timesheetapprovalrequiredbydefault` | boolean | no |  |
| `populatedefaultprojectmembers` | boolean | no | Defaults to true. |
| `istaskrequiredontimesheet` | boolean | no |  |
| `startdate` | date | no |  |
| `enddate` | date | no |  |
| `budgetamount` | number | no |  |
| `budgethours` | number | no |  |
| `projectstatuscode` | string | no |  |
| `projectcategoryidfk` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `POST /api/Project` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

