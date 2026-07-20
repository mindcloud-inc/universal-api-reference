# MessageBird: Get Channel



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-channel?connectionId=$CONNECTION_ID&workspaceId=string&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-channel?${params}`, {
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
| `workspaceId` | string | yes | The Bird workspace ID that owns the channel. |
| `channelId` | string | yes | The Bird channel ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capabilities": {},
      "channelMessageType": "string",
      "connectionParams": [
        {}
      ],
      "connectorId": "string",
      "contactIdentifierFormatOverride": {},
      "contactIdentifierKeyOverride": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "identifier": "string",
      "name": "Ava Chen",
      "platformId": "string",
      "platformMessageJsonSchemaOverride": {},
      "platformServiceProtocolOverride": "string",
      "platformServiceUrlOverride": "https://example.com",
      "platformServiceVersionOverride": "string",
      "platformTemplateEngineOverride": "string",
      "preferences": {},
      "resourceOwners": {},
      "settings": [
        {}
      ],
      "status": "string",
      "suites": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "useCaseId": "string",
      "useCaseType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capabilities` | object |  |
| `channelMessageType` | string |  |
| `connectionParams` | array<object> |  |
| `connectorId` | string |  |
| `contactIdentifierFormatOverride` | object |  |
| `contactIdentifierKeyOverride` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `identifier` | string |  |
| `name` | string |  |
| `platformId` | string |  |
| `platformMessageJsonSchemaOverride` | object |  |
| `platformServiceProtocolOverride` | string |  |
| `platformServiceUrlOverride` | string |  |
| `platformServiceVersionOverride` | string |  |
| `platformTemplateEngineOverride` | string |  |
| `preferences` | object |  |
| `resourceOwners` | object | The map of resource owners that are allowed to use this channel. Example:  { "resourceOwnerIdentifier1": { "id": "resourceOwnerUUID1", "type": "user" },    "resourceOwnerIdentifier2": { "id": "resourceOwnerUUID2", "type": "group" } } |
| `settings` | array<object> |  |
| `status` | string |  |
| `suites` | array<string> |  |
| `updatedAt` | date |  |
| `useCaseId` | string |  |
| `useCaseType` | string |  |

## Native endpoint

Through the native MessageBird API, this operation is `GET /workspaces/:workspaceId/channels/:channelId` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.

