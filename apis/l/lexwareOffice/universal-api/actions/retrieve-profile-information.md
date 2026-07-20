# Lexware Office: Retrieve Profile Information

Retrieves profile information from Lexware Office.

```
GET https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-profile-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-profile-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-profile-information?${params}`, {
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
      "businessFeatures": [
        "string"
      ],
      "connectionId": "string",
      "created": {
        "date": "2026-05-07T12:00:00.000Z",
        "userEmail": "ava@example.com",
        "userId": "string",
        "userName": "Ava Chen"
      },
      "organizationId": "string",
      "smallBusiness": true,
      "taxType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessFeatures` | array<string> | Enabled business features for the account. |
| `connectionId` | string | Lexware connection identifier. |
| `created` | object | Audit information for the profile connection. |
| `created.date` | date | Creation timestamp. |
| `created.userEmail` | string | User email that created the profile connection. |
| `created.userId` | string | User identifier that created the profile connection. |
| `created.userName` | string | User name that created the profile connection. |
| `organizationId` | string | Lexware organization identifier. |
| `smallBusiness` | boolean | Whether the account is marked as a small business. |
| `taxType` | string | Configured tax handling mode. |

## Native endpoint

Through the native Lexware Office API, this operation is `GET /v1/profile` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-profile-information.md) for the provider-specific parameters and requirements.

