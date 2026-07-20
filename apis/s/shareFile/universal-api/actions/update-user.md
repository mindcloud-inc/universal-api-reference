# ShareFile: Update User



```
PUT https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ShareFile user identifier to update. |
| `Email` | string | no | The email address for the ShareFile user. |
| `FirstName` | string | no | The first name of the ShareFile user. |
| `LastName` | string | no | The last name of the ShareFile user. |
| `Company` | string | no | The company name for the ShareFile user. |

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
      "IsAdmin": true,
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
| `IsAdmin` | boolean |  |
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

Through the native ShareFile API, this operation is `PATCH /Users({{id}})` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

