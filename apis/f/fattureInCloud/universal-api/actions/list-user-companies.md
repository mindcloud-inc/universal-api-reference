# Fatture in Cloud: List User Companies

Retrieves the user's companies from Fatture in Cloud.

```
GET https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/list-user-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fatture in Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/list-user-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/list-user-companies?${params}`, {
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
      "connectionId": 1,
      "connectionRole": "string",
      "dic": true,
      "dicPlan": 1,
      "email": "ava@example.com",
      "fic": true,
      "ficLicenseExpire": "2026-05-07T12:00:00.000Z",
      "ficPlan": "string",
      "id": 1,
      "name": "Ava Chen",
      "permissions": {
        "dicEmployees": "string",
        "dicSettings": "string",
        "dicTimesheet": "string",
        "ficArchive": "string",
        "ficCalendar": "string",
        "ficCashbook": "string",
        "ficClients": "string",
        "ficEmails": "ava@example.com",
        "ficIssuedDocuments": "string",
        "ficProducts": "string",
        "ficReceipts": "string",
        "ficReceivedDocuments": "string",
        "ficSettings": "string",
        "ficSituation": "string",
        "ficStock": "string",
        "ficSuppliers": "string",
        "ficTaxes": "string"
      },
      "taxCode": "string",
      "type": "string",
      "vatNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectionId` | number |  |
| `connectionRole` | string |  |
| `dic` | boolean |  |
| `dicPlan` | number |  |
| `email` | string |  |
| `fic` | boolean |  |
| `ficLicenseExpire` | date |  |
| `ficPlan` | string |  |
| `id` | number |  |
| `name` | string |  |
| `permissions.dicEmployees` | string |  |
| `permissions.dicSettings` | string |  |
| `permissions.dicTimesheet` | string |  |
| `permissions.ficArchive` | string |  |
| `permissions.ficCalendar` | string |  |
| `permissions.ficCashbook` | string |  |
| `permissions.ficClients` | string |  |
| `permissions.ficEmails` | string |  |
| `permissions.ficIssuedDocuments` | string |  |
| `permissions.ficProducts` | string |  |
| `permissions.ficReceipts` | string |  |
| `permissions.ficReceivedDocuments` | string |  |
| `permissions.ficSettings` | string |  |
| `permissions.ficSituation` | string |  |
| `permissions.ficStock` | string |  |
| `permissions.ficSuppliers` | string |  |
| `permissions.ficTaxes` | string |  |
| `taxCode` | string |  |
| `type` | string |  |
| `vatNumber` | string |  |

## Native endpoint

Through the native Fatture in Cloud API, this operation is `GET /user/companies` (base URL `https://api-v2.fattureincloud.it`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-companies.md) for the provider-specific parameters and requirements.

