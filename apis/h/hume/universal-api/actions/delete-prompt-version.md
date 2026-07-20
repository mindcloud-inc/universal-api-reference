# Hume: Delete prompt version



```
DELETE https://connect.mindcloud.co/v1/universal/hume/latest/actions/delete-prompt-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hume/latest/actions/delete-prompt-version?connectionId=$CONNECTION_ID&id=string&version=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "version": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hume/latest/actions/delete-prompt-version?${params}`, {
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
| `id` | string | yes | EVI prompt identifier. |
| `version` | number | yes | Version number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native Hume API, this operation is `DELETE /v0/evi/prompts/:id/version/:version` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-prompt-version.md) for the provider-specific parameters and requirements.

