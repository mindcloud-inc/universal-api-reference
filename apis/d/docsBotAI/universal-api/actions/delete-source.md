# DocsBot AI: Delete Source

Deletes an existing source from DocsBot AI.

```
DELETE https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/delete-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocsBot AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/delete-source?connectionId=$CONNECTION_ID&botId=string&sourceId=string&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string",
  "sourceId": "string",
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docsBotAI/latest/actions/delete-source?${params}`, {
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
| `botId` | string | yes | The DocsBot bot ID. |
| `sourceId` | string | yes | The DocsBot source ID. |
| `teamId` | string | yes | The DocsBot team ID. |

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

Through the native DocsBot AI API, this operation is `DELETE /teams/:teamId/bots/:botId/sources/:sourceId` (base URL `https://docsbot.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-source.md) for the provider-specific parameters and requirements.

