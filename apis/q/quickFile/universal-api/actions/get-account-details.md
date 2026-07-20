# QuickFile: Get Account Details



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-account-details?${params}`, {
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
      "accountNumber": "string",
      "address": "string",
      "backupSchedule": {},
      "baseCurrency": "string",
      "businessType": "string",
      "clientDomain": "string",
      "companyName": "Ava Chen",
      "companyNumber": "string",
      "countryIso": "string",
      "dailyDataTransferLimit": 1,
      "teamMembers": {},
      "tel": "string",
      "vatRegNumber": "string",
      "web": "string",
      "yearEndDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountNumber` | string |  |
| `address` | string |  |
| `backupSchedule` | object |  |
| `baseCurrency` | string |  |
| `businessType` | string |  |
| `clientDomain` | string |  |
| `companyName` | string |  |
| `companyNumber` | string |  |
| `countryIso` | string |  |
| `dailyDataTransferLimit` | number |  |
| `teamMembers` | object |  |
| `tel` | string |  |
| `vatRegNumber` | string |  |
| `web` | string |  |
| `yearEndDate` | date |  |

## Native endpoint

Through the native QuickFile API, this operation is `POST /system/getaccountdetails` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.

