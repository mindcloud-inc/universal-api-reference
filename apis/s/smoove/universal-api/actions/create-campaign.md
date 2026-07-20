# Smoove: Create Campaign

Creates a new email campaign in Smoove.

```
POST https://connect.mindcloud.co/v1/universal/smoove/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smoove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smoove/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smoove/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | no |  |
| `body` | string | no |  |
| `toMembersByEmail[]` | array<string> | no |  |
| `toMembersByExternalId[]` | array<string> | no |  |
| `toMembersById[]` | array<number> | no |  |
| `toListsById[]` | array<number> | no |  |
| `excludeFromMembers[]` | array<number> | no |  |
| `excludeFromLists[]` | array<number> | no |  |
| `trackLinks` | boolean | no |  |
| `customUnsubscribeMode` | list | no | One of: `None`, `PingAndUnsubscribe`, `PingOnly`, `RedirectAndUnsubscribe`, `RedirectOnly`. Default: `None`. |
| `externalUnsubscribeUrl` | string | no |  |
| `customData[]` | array<object> | no |  |
| `campaignAttachments[]` | array<string> | no |  |
| `externalId` | string | no |  |
| `customFromAddress` | string | no |  |
| `customReplyToAddress` | string | no |  |
| `sendNow` | boolean | no |  |
| `scheduleTo` | string | no |  |
| `templateName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customUnsubscribeMode": "string",
      "id": 1,
      "subject": "string",
      "trackLinks": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customUnsubscribeMode` | string |  |
| `id` | number |  |
| `subject` | string |  |
| `trackLinks` | boolean |  |

## Native endpoint

Through the native Smoove API, this operation is `POST /v1/Campaigns` (base URL `https://rest.smoove.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

