# Zoho Cliq: List Channel Members

Retrieves members of a Zoho Cliq channel.

```
GET https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-channel-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-channel-members?connectionId=$CONNECTION_ID&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-channel-members?${params}`, {
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
| `channelId` | string | yes | The ID of the channel whose members should be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "members": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `members` | array<object> |  |

## Native endpoint

Through the native Zoho Cliq API, this operation is `GET /channels/:channelId/members` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-members.md) for the provider-specific parameters and requirements.

