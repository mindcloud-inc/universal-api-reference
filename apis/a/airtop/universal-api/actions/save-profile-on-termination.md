# Airtop: Save Profile On Termination

Saves a named profile when an Airtop session terminates.

```
PUT https://connect.mindcloud.co/v1/universal/airtop/latest/actions/save-profile-on-termination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airtop/latest/actions/save-profile-on-termination" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string",
  "profileName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airtop/latest/actions/save-profile-on-termination', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string",
    "profileName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes |  |
| `profileName` | string | yes | Name under which to save the profile |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airtop API returns.

## Native endpoint

Through the native Airtop API, this operation is `PUT /sessions/:sessionId/save-profile-on-termination/:profileName` (base URL `https://api.airtop.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-profile-on-termination.md) for the provider-specific parameters and requirements.

