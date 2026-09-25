# Microsoft Entra: List Group Memberships



```
GET https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-group-memberships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Entra `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-group-memberships?connectionId=$CONNECTION_ID&limit=25&offset=0&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/list-group-memberships?${params}`, {
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
| `filter` | string | no | OData filter expression; requires Include Count. |
| `groupId` | list<string> | yes |  |
| `search` | string | no | Search displayName or description; requires Include Count. |
| `count` | boolean | no | Required for advanced directory queries. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no | Comma-separated property names. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classification": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "deletedDateTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "displayName": "Ava Chen",
      "expirationDateTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isAssignableToRole": true,
      "mail": "ava@example.com",
      "mailEnabled": true,
      "mailNickname": "Ava Chen",
      "membershipRule": "string",
      "membershipRuleProcessingState": "string",
      "onPremisesDomainName": "Ava Chen",
      "onPremisesLastSyncDateTime": "2026-05-07T12:00:00.000Z",
      "onPremisesNetBiosName": "Ava Chen",
      "onPremisesSamAccountName": "Ava Chen",
      "onPremisesSecurityIdentifier": "string",
      "onPremisesSyncEnabled": true,
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
| `deletedDateTime` | date |  |
| `description` | string |  |
| `displayName` | string |  |
| `expirationDateTime` | date |  |
| `id` | string |  |
| `isAssignableToRole` | boolean |  |
| `mail` | string |  |
| `mailEnabled` | boolean |  |
| `mailNickname` | string |  |
| `membershipRule` | string |  |
| `membershipRuleProcessingState` | string |  |
| `onPremisesDomainName` | string |  |
| `onPremisesLastSyncDateTime` | date |  |
| `onPremisesNetBiosName` | string |  |
| `onPremisesSamAccountName` | string |  |
| `onPremisesSecurityIdentifier` | string |  |
| `onPremisesSyncEnabled` | boolean |  |
| `preferredDataLocation` | string |  |
| `preferredLanguage` | string |  |
| `renewedDateTime` | date |  |
| `securityEnabled` | boolean |  |
| `securityIdentifier` | string |  |
| `theme` | string |  |
| `uniqueName` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Microsoft Entra API, this operation is `GET /groups/:groupId/memberOf` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-group-memberships.md) for the provider-specific parameters and requirements.

