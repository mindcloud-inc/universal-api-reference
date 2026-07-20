# Quantum Digital: Get Account Extra Data



```
GET https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/get-account-extra-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quantum Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/get-account-extra-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quantumDigital/latest/actions/get-account-extra-data?${params}`, {
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
      "allowProductionMode": true,
      "apiModeId": 1,
      "assocApiAccountId": 1,
      "clientId": "string",
      "dashboardAccountName": "Ava Chen",
      "firstTimeUser": true,
      "isInternalDevCompany": true,
      "loginEmail": "ava@example.com",
      "loginHint": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowProductionMode` | boolean | Whether production mode is available. |
| `apiModeId` | number | Current API account mode identifier. |
| `assocApiAccountId` | number | Associated API account identifier. |
| `clientId` | string | Provider client identifier. |
| `dashboardAccountName` | string | Dashboard account display name. |
| `firstTimeUser` | boolean | Whether this is a first-time user. |
| `isInternalDevCompany` | boolean | Whether the account belongs to an internal dev company. |
| `loginEmail` | string | Login email address. |
| `loginHint` | string | Login hint returned by the provider. |

## Native endpoint

Through the native Quantum Digital API, this operation is `GET /devplatform/accounts/:dashboardAccountId` (base URL `https://api.quantumdigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-extra-data.md) for the provider-specific parameters and requirements.

