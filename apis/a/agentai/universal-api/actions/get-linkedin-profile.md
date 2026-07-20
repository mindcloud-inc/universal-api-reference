# Agent.ai: Get LinkedIn Profile

Retrieves a LinkedIn profile from Agent.ai by handle.

```
GET https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-linkedin-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-linkedin-profile?connectionId=$CONNECTION_ID&profileHandle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileHandle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-linkedin-profile?${params}`, {
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
| `profileHandle` | string | yes | LinkedIn profile handle to retrieve details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object | LinkedIn profile data. |
| `status` | number | HTTP status code of the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/get_linkedin_profile` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-linkedin-profile.md) for the provider-specific parameters and requirements.

