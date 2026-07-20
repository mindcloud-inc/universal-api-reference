# Follow Up Boss: Get Current User

Retrieves the current user from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-current-user?${params}`, {
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
      "account": 1,
      "algoliaAppId": "string",
      "algoliaKey": "string",
      "beta": true,
      "betaOnly": true,
      "callingBehavior": "string",
      "callingEnabled": true,
      "callingPhoneNumberCanText": true,
      "canCreateApiKeys": true,
      "canExport": true,
      "capabilities": {},
      "connectedEmail": {},
      "created": "string",
      "email": "ava@example.com",
      "emailConnectivity": {},
      "features": [
        "string"
      ],
      "firstName": "Ava",
      "fuid": "string",
      "id": 1,
      "isOwner": true,
      "lastName": "Chen",
      "leadEmailAddress": "ava@example.com",
      "name": "Ava Chen",
      "notifyAboutAllLeads": true,
      "notifyBy": [
        "string"
      ],
      "outboundNumber": "string",
      "phone": "string",
      "picture": {},
      "rawSignature": "string",
      "role": "string",
      "shareAppointments": true,
      "shareEmails": true,
      "signature": "string",
      "teamIds": [
        1
      ],
      "teamLeaderOf": [
        1
      ],
      "teamMember": {},
      "textingEnabled": true,
      "timeZone": "string",
      "typesenseEndpoints": [
        "string"
      ],
      "typesenseKey": "string",
      "unreadConversationCount": 1,
      "updated": "string",
      "vcard": {},
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | number |  |
| `algoliaAppId` | string |  |
| `algoliaKey` | string |  |
| `beta` | boolean |  |
| `betaOnly` | boolean |  |
| `callingBehavior` | string |  |
| `callingEnabled` | boolean |  |
| `callingPhoneNumberCanText` | boolean |  |
| `canCreateApiKeys` | boolean |  |
| `canExport` | boolean |  |
| `capabilities` | object |  |
| `connectedEmail` | object |  |
| `created` | string |  |
| `email` | string |  |
| `emailConnectivity` | object |  |
| `features` | array<string> |  |
| `firstName` | string |  |
| `fuid` | string |  |
| `id` | number |  |
| `isOwner` | boolean |  |
| `lastName` | string |  |
| `leadEmailAddress` | string |  |
| `name` | string |  |
| `notifyAboutAllLeads` | boolean |  |
| `notifyBy` | array<string> |  |
| `outboundNumber` | string |  |
| `phone` | string |  |
| `picture` | object |  |
| `rawSignature` | string |  |
| `role` | string |  |
| `shareAppointments` | boolean |  |
| `shareEmails` | boolean |  |
| `signature` | string |  |
| `teamIds` | array<number> |  |
| `teamLeaderOf` | array<number> |  |
| `teamMember` | object |  |
| `textingEnabled` | boolean |  |
| `timeZone` | string |  |
| `typesenseEndpoints` | array<string> |  |
| `typesenseKey` | string |  |
| `unreadConversationCount` | number |  |
| `updated` | string |  |
| `vcard` | object |  |
| `version` | number |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `GET me` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

