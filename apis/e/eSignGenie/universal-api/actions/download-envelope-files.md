# eSign Genie: Download Envelope Files

Retrieves envelope files from eSign Genie.

```
GET https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/download-envelope-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eSign Genie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/download-envelope-files?connectionId=$CONNECTION_ID&folderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSignGenie/latest/actions/download-envelope-files?${params}`, {
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
| `folderId` | number | yes | The Foxit eSign envelope ID whose files should be downloaded. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eSign Genie API returns.

## Native endpoint

Through the native eSign Genie API, this operation is `GET /folders/download` (base URL `https://na1.foxitesign.foxit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-envelope-files.md) for the provider-specific parameters and requirements.

