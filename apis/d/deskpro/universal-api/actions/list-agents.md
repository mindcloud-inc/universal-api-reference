# Deskpro: List Agents

Retrieves a list of agents from Deskpro.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-agents?${params}`, {
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
      "agentData": {
        "agentCallsEnabled": true,
        "agentCanUseForwarding": true,
        "agentChatEnabled": true,
        "agentType": "string",
        "availableStatus": "string",
        "forwardingLoggedOut": true,
        "forwardingNumber": "string",
        "forwardingNumberType": "string",
        "forwardingRingTimeout": 1,
        "lastOnline": "2026-05-07T12:00:00.000Z",
        "loginStatus": "string",
        "workStatusEnabled": true
      },
      "avatar": {
        "defaultUrlPattern": "https://example.com"
      },
      "displayName": "Ava Chen",
      "firstName": "Ava",
      "id": 1,
      "isAgent": true,
      "lastName": "Chen",
      "lastSeen": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "online": true,
      "onlineForChat": true,
      "primaryEmail": "ava@example.com",
      "titlePrefix": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentData.agentCallsEnabled` | boolean |  |
| `agentData.agentCanUseForwarding` | boolean |  |
| `agentData.agentChatEnabled` | boolean |  |
| `agentData.agentType` | string |  |
| `agentData.availableStatus` | string |  |
| `agentData.forwardingLoggedOut` | boolean |  |
| `agentData.forwardingNumber` | string |  |
| `agentData.forwardingNumberType` | string |  |
| `agentData.forwardingRingTimeout` | number |  |
| `agentData.lastOnline` | date |  |
| `agentData.loginStatus` | string |  |
| `agentData.workStatusEnabled` | boolean |  |
| `avatar.defaultUrlPattern` | string |  |
| `displayName` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `isAgent` | boolean |  |
| `lastName` | string |  |
| `lastSeen` | date |  |
| `name` | string |  |
| `online` | boolean |  |
| `onlineForChat` | boolean |  |
| `primaryEmail` | string |  |
| `titlePrefix` | string |  |

## Native endpoint

Through the native Deskpro API, this operation is `GET /agents` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

