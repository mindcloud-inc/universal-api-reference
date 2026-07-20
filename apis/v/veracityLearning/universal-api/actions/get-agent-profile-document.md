# Veracity Learning: Get Agent Profile Document

Retrieves an agent profile document from Veracity Learning.

```
GET https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-agent-profile-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-agent-profile-document?connectionId=$CONNECTION_ID&agent=%5Bobject%20Object%5D&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agent": "[object Object]",
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/get-agent-profile-document?${params}`, {
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
| `agent` | object | yes | Agent object whose profile document should be loaded |
| `profileId` | string | yes | Profile id to load |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Veracity Learning API returns.

## Native endpoint

Through the native Veracity Learning API, this operation is `GET /agents/profile` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-profile-document.md) for the provider-specific parameters and requirements.

