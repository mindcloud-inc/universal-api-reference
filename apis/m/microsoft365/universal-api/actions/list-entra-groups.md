# Microsoft 365: List Entra Groups

Retrieves Entra groups from Microsoft 365.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-entra-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-entra-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-entra-groups?${params}`, {
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
| `filter` | string | no | User OData filters on the dataset |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classification": {},
      "createdDateTime": "string",
      "deletedDateTime": {},
      "description": "string",
      "displayName": "Ava Chen",
      "expirationDateTime": {},
      "id": "string",
      "isAssignableToRole": {},
      "mail": "string",
      "mailEnabled": true,
      "mailNickname": "Ava Chen",
      "membershipRule": {},
      "membershipRuleProcessingState": {},
      "onPremisesDomainName": {},
      "onPremisesLastSyncDateTime": {},
      "onPremisesNetBiosName": {},
      "onPremisesSamAccountName": {},
      "onPremisesSecurityIdentifier": {},
      "onPremisesSyncEnabled": {},
      "preferredDataLocation": {},
      "preferredLanguage": {},
      "proxyAddresses": [
        "string"
      ],
      "renewedDateTime": "string",
      "securityEnabled": true,
      "securityIdentifier": "string",
      "theme": {},
      "uniqueName": {},
      "visibility": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classification` | object |  |
| `createdDateTime` | string |  |
| `deletedDateTime` | object |  |
| `description` | string |  |
| `displayName` | string |  |
| `expirationDateTime` | object |  |
| `id` | string |  |
| `isAssignableToRole` | object |  |
| `mail` | string |  |
| `mailEnabled` | boolean |  |
| `mailNickname` | string |  |
| `membershipRule` | object |  |
| `membershipRuleProcessingState` | object |  |
| `onPremisesDomainName` | object |  |
| `onPremisesLastSyncDateTime` | object |  |
| `onPremisesNetBiosName` | object |  |
| `onPremisesSamAccountName` | object |  |
| `onPremisesSecurityIdentifier` | object |  |
| `onPremisesSyncEnabled` | object |  |
| `preferredDataLocation` | object |  |
| `preferredLanguage` | object |  |
| `proxyAddresses[]` | string |  |
| `renewedDateTime` | string |  |
| `securityEnabled` | boolean |  |
| `securityIdentifier` | string |  |
| `theme` | object |  |
| `uniqueName` | object |  |
| `visibility` | object |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `GET /v1.0/groups` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-entra-groups.md) for the provider-specific parameters and requirements.

