# Microsoft Entra: Get Group



```
GET https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Entra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/get-group?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftEntra/latest/actions/get-group?${params}`, {
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
| `groupId` | list<string> | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `select` | string | no |  |
| `expand` | string | no |  |

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

Through the native Microsoft Entra API, this operation is `GET /groups/:groupId` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

