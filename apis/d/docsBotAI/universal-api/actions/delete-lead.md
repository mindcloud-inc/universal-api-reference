# DocsBot AI: Delete Lead

Deletes an existing lead from DocsBot AI.

```
DELETE https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/delete-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocsBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/delete-lead?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/delete-lead?${params}`, {
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

Through the native DocsBot AI API, this operation is `DELETE /teams/:teamId/bots/:botId/leads/:leadId` (base URL `https://docsbot.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-lead.md) for the provider-specific parameters and requirements.

