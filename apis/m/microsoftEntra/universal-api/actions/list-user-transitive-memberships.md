# Microsoft Entra: List User Transitive Memberships



```
GET https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-user-transitive-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Entra `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-user-transitive-memberships?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=87d349ed-44d7-43e1-9a83-5f2406dee5bd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "87d349ed-44d7-43e1-9a83-5f2406dee5bd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-user-transitive-memberships?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | list<string> | yes | Example: `87d349ed-44d7-43e1-9a83-5f2406dee5bd`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated properties, such as id,displayName. Example: `id,displayName`. |
| `filter` | string | no | OData filter expression. Advanced queries require Include Count. Example: `startsWith(displayName,'A')`. |
| `search` | string | no | Search expression, such as "displayName:Ava". Requires Include Count. Example: `"displayName:Ava"`. |
| `count` | boolean | no | Include the matching count. Required for advanced search, filtering, and sorting. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classification": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "deletedDateTime": "string",
      "description": "string",
      "displayName": "Ava Chen",
      "expirationDateTime": "string",
      "id": "string",
      "isAssignableToRole": "string",
      "mail": "ava@example.com",
      "mailEnabled": true,
      "mailNickname": "Ava Chen",
      "membershipRule": "string",
      "membershipRuleProcessingState": "string",
      "onPremisesDomainName": "Ava Chen",
      "onPremisesLastSyncDateTime": "string",
      "onPremisesNetBiosName": "Ava Chen",
      "onPremisesSamAccountName": "Ava Chen",
      "onPremisesSecurityIdentifier": "string",
      "onPremisesSyncEnabled": "string",
      "preferredDataLocation": "string",
      "preferredLanguage": "string",
      "renewedDateTime": "2026-05-07T12:00:00.000Z",
      "securityEnabled": true,
      "securityIdentifier": "string",
      "theme": "string",
      "uniqueName": "Ava Chen",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classification` | string |  |
| `createdDateTime` | date |  |
| `deletedDateTime` | string |  |
| `description` | string |  |
| `displayName` | string |  |
| `expirationDateTime` | string |  |
| `id` | string |  |
| `isAssignableToRole` | string |  |
| `mail` | string |  |
| `mailEnabled` | boolean |  |
| `mailNickname` | string |  |
| `membershipRule` | string |  |
| `membershipRuleProcessingState` | string |  |
| `onPremisesDomainName` | string |  |
| `onPremisesLastSyncDateTime` | string |  |
| `onPremisesNetBiosName` | string |  |
| `onPremisesSamAccountName` | string |  |
| `onPremisesSecurityIdentifier` | string |  |
| `onPremisesSyncEnabled` | string |  |
| `preferredDataLocation` | string |  |
| `preferredLanguage` | string |  |
| `renewedDateTime` | date |  |
| `securityEnabled` | boolean |  |
| `securityIdentifier` | string |  |
| `theme` | string |  |
| `uniqueName` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Microsoft Entra API, this operation is `GET /users/:userId/transitiveMemberOf` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-transitive-memberships.md) for the provider-specific parameters and requirements.

