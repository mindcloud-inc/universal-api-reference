# PrintNode: Get Latest Client Download

Retrieves the latest client download from PrintNode by operating system.

```
GET https://connect.mindcloud.co/v1/universal/printNode/latest/actions/get-latest-client-download
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/get-latest-client-download?connectionId=$CONNECTION_ID&operatingSystem=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "operatingSystem": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printNode/latest/actions/get-latest-client-download?${params}`, {
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
| `operatingSystem` | string | yes | Operating system token from the PrintNode download docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "edition": "string",
      "filename": "Ava Chen",
      "filesize": 1,
      "releaseTimestamp": "2026-05-07T12:00:00.000Z",
      "sha1": "string",
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `edition` | string | PrintNode client edition name. |
| `filename` | string | Download filename. |
| `filesize` | number | Download file size in bytes. |
| `releaseTimestamp` | date | Release timestamp for the latest client build. |
| `sha1` | string | SHA1 digest of the latest client build. |
| `url` | string | Latest client download URL returned by PrintNode. |
| `version` | string | Client version. |

## Native endpoint

Through the native PrintNode API, this operation is `GET /download/client/:operatingSystem` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-client-download.md) for the provider-specific parameters and requirements.

