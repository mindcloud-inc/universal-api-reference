# Phonely: Delete Agent Websites

Deletes agent websites from Phonely.

```
DELETE https://connect.mindcloud.co/v1/universal/phonely/latest/actions/delete-agent-websites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/delete-agent-websites?connectionId=$CONNECTION_ID&uid=string&agentId=string&websiteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string",
  "agentId": "string",
  "websiteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phonely/latest/actions/delete-agent-websites?${params}`, {
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
| `uid` | string | yes |  |
| `agentId` | string | yes |  |
| `websiteId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Phonely API, this operation is `DELETE /api/agent-websites` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-agent-websites.md) for the provider-specific parameters and requirements.

