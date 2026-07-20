# Maildrip: Get details about a specific tool



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-details-about-a-specific-tool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-details-about-a-specific-tool?connectionId=$CONNECTION_ID&toolName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "toolName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-details-about-a-specific-tool?${params}`, {
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
| `toolName` | string | yes | Name of the tool to get details for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tool": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tool` | object |  |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/mcp/tools/{toolName}` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-details-about-a-specific-tool.md) for the provider-specific parameters and requirements.

