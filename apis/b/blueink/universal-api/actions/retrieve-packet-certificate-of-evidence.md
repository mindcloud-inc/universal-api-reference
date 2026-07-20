# Blueink: Retrieve Packet Certificate of Evidence

Retrieves a packet certificate of evidence from Blueink.

```
GET https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-packet-certificate-of-evidence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-packet-certificate-of-evidence?connectionId=$CONNECTION_ID&packetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-packet-certificate-of-evidence?${params}`, {
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
| `packetId` | string | yes | Packet ID to retrieve the certificate of evidence for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires": "2026-05-07T12:00:00.000Z",
      "fileUrl": "https://example.com",
      "sha256": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires` | date |  |
| `fileUrl` | string |  |
| `sha256` | string |  |

## Native endpoint

Through the native Blueink API, this operation is `GET /packets/:packetId/coe/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-packet-certificate-of-evidence.md) for the provider-specific parameters and requirements.

