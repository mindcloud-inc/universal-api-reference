# Docage: List Docage Users

Retrieves accessible users from Docage.

```
GET https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-docage-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-docage-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-docage-users?${params}`, {
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
      "AlertEnabled": true,
      "ApplicationUserId": "string",
      "Company": "string",
      "CourrierEnabled": true,
      "EbpUserName": "Ava Chen",
      "Email": "ava@example.com",
      "FirstName": "Ava",
      "GdprEnabled": true,
      "Gender": 1,
      "Job": "string",
      "Language": 1,
      "LastName": "Chen",
      "SignatureEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AlertEnabled` | boolean |  |
| `ApplicationUserId` | string |  |
| `Company` | string |  |
| `CourrierEnabled` | boolean |  |
| `EbpUserName` | string |  |
| `Email` | string |  |
| `FirstName` | string |  |
| `GdprEnabled` | boolean |  |
| `Gender` | number |  |
| `Job` | string |  |
| `Language` | number |  |
| `LastName` | string |  |
| `SignatureEnabled` | boolean |  |

## Native endpoint

Through the native Docage API, this operation is `GET /DocageUsers` (base URL `https://api.docage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-docage-users.md) for the provider-specific parameters and requirements.

