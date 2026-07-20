# Ortto: List Audiences



```
GET https://connect.mindcloud.co/v1/universal/ortto/latest/actions/list-audiences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/list-audiences?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ortto/latest/actions/list-audiences?${params}`, {
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
| `searchTerm` | string | no | Audience search term. |
| `withFilter` | boolean | no | Only return audiences with a filter configured. |
| `archived` | boolean | no | Include archived audiences. |
| `retention` | string | no | Audience retention type. |
| `limit` | number | no | Maximum number of audiences to return. |
| `offset` | number | no | Number of audiences to skip. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedLast30Days": 1,
      "associatedContacts": 1,
      "building": true,
      "created": "string",
      "createdById": "string",
      "createdByName": "Ava Chen",
      "dataSourceId": "string",
      "dsDestinations": {},
      "editedAt": "string",
      "editedById": "string",
      "editedByName": "Ava Chen",
      "engagement": 1,
      "exitSelection": "string",
      "filter": {},
      "filterSha": "string",
      "folderId": {},
      "iconId": "string",
      "id": "string",
      "instanceId": "string",
      "isCold": true,
      "isPublic": true,
      "lastBuiltAt": "string",
      "lastUsed": "string",
      "members": 1,
      "name": "Ava Chen",
      "newExitCriteriaFilter": {},
      "newFilter": {},
      "newFilterSha": "string",
      "publicDescription": "string",
      "publicName": "Ava Chen",
      "ready": true,
      "revenue": 1,
      "smsIsPublic": true,
      "smsOptedIn": 1,
      "smsPublicDescription": "string",
      "smsPublicName": "Ava Chen",
      "subscribers": 1,
      "templateId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedLast30Days` | number |  |
| `associatedContacts` | number |  |
| `building` | boolean |  |
| `created` | string |  |
| `createdById` | string |  |
| `createdByName` | string |  |
| `dataSourceId` | string |  |
| `dsDestinations` | object |  |
| `editedAt` | string |  |
| `editedById` | string |  |
| `editedByName` | string |  |
| `engagement` | number |  |
| `exitSelection` | string |  |
| `filter` | object |  |
| `filterSha` | string |  |
| `folderId` | object |  |
| `iconId` | string |  |
| `id` | string |  |
| `instanceId` | string |  |
| `isCold` | boolean |  |
| `isPublic` | boolean |  |
| `lastBuiltAt` | string |  |
| `lastUsed` | string |  |
| `members` | number |  |
| `name` | string |  |
| `newExitCriteriaFilter` | object |  |
| `newFilter` | object |  |
| `newFilterSha` | string |  |
| `publicDescription` | string |  |
| `publicName` | string |  |
| `ready` | boolean |  |
| `revenue` | number |  |
| `smsIsPublic` | boolean |  |
| `smsOptedIn` | number |  |
| `smsPublicDescription` | string |  |
| `smsPublicName` | string |  |
| `subscribers` | number |  |
| `templateId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /audiences/get` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-audiences.md) for the provider-specific parameters and requirements.

