# Zahara: List Projects

Retrieves projects from a Zahara business unit.

```
GET https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-projects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "Address": {
        "AddressId": 1,
        "AddressLines": "string",
        "AddressType": 1,
        "CountryCode": "string",
        "CountryCodeId": 1,
        "IsPrimary": true,
        "LastUpdated": "2026-05-07T12:00:00.000Z",
        "Postcode": "string",
        "Void": true
      },
      "BudgetedAmount": 1,
      "BusinessUnitId": 1,
      "DateCreated": "2026-05-07T12:00:00.000Z",
      "Description": "string",
      "End": "2026-05-07T12:00:00.000Z",
      "LastUpdated": "2026-05-07T12:00:00.000Z",
      "ProjectCode": "string",
      "ProjectId": 1,
      "ProjectIncome": 1,
      "ProjectName": "Ava Chen",
      "ProjectRestrictionSettings": {
        "NominalsRestrictionPriorityType": 1,
        "RestrictNominals": true,
        "SetNominalsAsBudget": true
      },
      "Start": "2026-05-07T12:00:00.000Z",
      "Status": 1,
      "Void": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address.AddressId` | number | Project address ID. |
| `Address.AddressLines` | string | Project address lines. |
| `Address.AddressType` | number | Project address type. |
| `Address.CountryCode` | string | Project country code. |
| `Address.CountryCodeId` | number | Project country code ID. |
| `Address.IsPrimary` | boolean | Whether the project address is primary. |
| `Address.LastUpdated` | date | Project address last update timestamp. |
| `Address.Postcode` | string | Project postcode. |
| `Address.Void` | boolean | Whether the project address is void. |
| `BudgetedAmount` | number | Budgeted amount. |
| `BusinessUnitId` | number | Business unit ID. |
| `DateCreated` | date | Creation timestamp. |
| `Description` | string | Project description. |
| `End` | date | Project end date. |
| `LastUpdated` | date | Last update timestamp. |
| `ProjectCode` | string | Project code. |
| `ProjectId` | number | Project ID. |
| `ProjectIncome` | number | Project income amount. |
| `ProjectName` | string | Project name. |
| `ProjectRestrictionSettings.NominalsRestrictionPriorityType` | number | Nominal restriction priority type. |
| `ProjectRestrictionSettings.RestrictNominals` | boolean | Whether nominal codes are restricted. |
| `ProjectRestrictionSettings.SetNominalsAsBudget` | boolean | Whether nominals are used as budget. |
| `Start` | date | Project start date. |
| `Status` | number | Project status. |
| `Void` | boolean | Whether the project is void. |

## Native endpoint

Through the native Zahara API, this operation is `GET /api/{{credentials.businessUnitApiKey}}/Project/GetAll` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

