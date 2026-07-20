# ShareFile: Create Client User



```
POST https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/create-client-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/create-client-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Email": "ava@example.com",
  "FirstName": "Ava",
  "LastName": "Chen",
  "Company": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/create-client-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Email": "ava@example.com",
    "FirstName": "Ava",
    "LastName": "Chen",
    "Company": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Email` | string | yes | The email address for the ShareFile user. |
| `FirstName` | string | yes | The first name of the ShareFile user. |
| `LastName` | string | yes | The last name of the ShareFile user. |
| `Company` | string | yes | The company name for the ShareFile user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Company": "string",
      "Contacted": 1,
      "DateCreated": "string",
      "Domain": "string",
      "Email": "ava@example.com",
      "EmailAddresses": [
        {}
      ],
      "Emails": [
        "ava@example.com"
      ],
      "FirstName": "Ava",
      "FullName": "Ava Chen",
      "FullNameShort": "Ava Chen",
      "Id": "string",
      "Initials": "string",
      "IsBillingContact": true,
      "IsConfirmed": true,
      "IsDeleted": true,
      "LastName": "Chen",
      "odata": {
        "metadata": "string",
        "type": "string"
      },
      "ReferredBy": "string",
      "Roles": [
        "string"
      ],
      "TotalSharedFiles": 1,
      "url": "https://example.com",
      "Username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Company` | string |  |
| `Contacted` | number |  |
| `DateCreated` | string |  |
| `Domain` | string |  |
| `Email` | string |  |
| `EmailAddresses` | array<object> |  |
| `Emails` | array<string> |  |
| `FirstName` | string |  |
| `FullName` | string |  |
| `FullNameShort` | string |  |
| `Id` | string |  |
| `Initials` | string |  |
| `IsBillingContact` | boolean |  |
| `IsConfirmed` | boolean |  |
| `IsDeleted` | boolean |  |
| `LastName` | string |  |
| `odata.metadata` | string |  |
| `odata.type` | string |  |
| `ReferredBy` | string |  |
| `Roles` | array<string> |  |
| `TotalSharedFiles` | number |  |
| `url` | string |  |
| `Username` | string |  |

## Native endpoint

Through the native ShareFile API, this operation is `POST /Users` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client-user.md) for the provider-specific parameters and requirements.

