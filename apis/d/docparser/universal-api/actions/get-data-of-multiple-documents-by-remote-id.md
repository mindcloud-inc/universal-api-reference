# Docparser: Get Data Of Multiple Documents By Remote ID

Retrieves parsed data for Docparser documents by remote ID.

```
GET https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-data-of-multiple-documents-by-remote-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-data-of-multiple-documents-by-remote-id?connectionId=$CONNECTION_ID&parserId=tiumtyrcddpn&remoteId=codex-stage3-1773346249-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parserId": "tiumtyrcddpn",
  "remoteId": "codex-stage3-1773346249-content"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-data-of-multiple-documents-by-remote-id?${params}`, {
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
| `parserId` | string | yes | Use the parser ID returned by List Document Parsers. Example: `tiumtyrcddpn`. |
| `remoteId` | string | yes | Return only parsed documents that match this remote ID. Example: `codex-stage3-1773346249-content`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeProcessingQueue` | boolean | no | Include documents that are still waiting in the processing queue. Example: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Docparser API returns.

## Native endpoint

Through the native Docparser API, this operation is `GET /v1/results/:PARSER_ID` (base URL `https://api.docparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-of-multiple-documents-by-remote-id.md) for the provider-specific parameters and requirements.

