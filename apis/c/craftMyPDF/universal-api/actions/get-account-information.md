# CraftMyPDF: Get account information

Retrieves account information from your CraftMyPDF account.

```
GET https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/get-account-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CraftMyPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/craftMyPDF/latest/actions/get-account-information?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "isTeam": true,
      "quotaCounter": 1,
      "quotaMax": 1,
      "status": "string",
      "templateCounter": 1,
      "templateMax": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Account creation timestamp. |
| `isTeam` | boolean | Whether the account is a team account. |
| `quotaCounter` | number | Current quota usage count. |
| `quotaMax` | number | Quota limit for the account. |
| `status` | string | CraftMyPDF response status. |
| `templateCounter` | number | Current template count. |
| `templateMax` | number | Maximum number of templates allowed. |
| `username` | string | CraftMyPDF account username. |

## Native endpoint

Through the native CraftMyPDF API, this operation is `GET /get-account-info` (base URL `https://api.craftmypdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-information.md) for the provider-specific parameters and requirements.

