# Bolna: Delete Knowledgebase

Deletes an existing knowledgebase from your Bolna account.

```
DELETE https://connect.mindcloud.co/v1/universal/bolna/latest/actions/delete-knowledgebase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/delete-knowledgebase?connectionId=$CONNECTION_ID&ragId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ragId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bolna/latest/actions/delete-knowledgebase?${params}`, {
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
| `ragId` | string | yes | The ID of the knowledgebase. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bolna API, this operation is `DELETE /knowledgebase/:ragId` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-knowledgebase.md) for the provider-specific parameters and requirements.

