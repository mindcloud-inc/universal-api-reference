# Veracity Learning: List Agent Profile IDs

Lists agent profile IDs from Veracity Learning.

```
GET https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-agent-profile-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-agent-profile-ids?connectionId=$CONNECTION_ID&agent=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agent": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/list-agent-profile-ids?${params}`, {
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
| `agent` | object | yes | Agent object whose profile ids should be listed |
| `since` | date | no | Only return profile ids updated since this timestamp |

## Response

```json
{
  "success": true,
  "data": [
    {
      "profileId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `profileId` | string | Agent profile document identifier available for the requested agent. |

## Native endpoint

Through the native Veracity Learning API, this operation is `GET /agents/profile` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agent-profile-ids.md) for the provider-specific parameters and requirements.

