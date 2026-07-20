# CINCEL: Get Timestamp Or Certificate Artifact



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-timestamp-or-certificate-artifact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-timestamp-or-certificate-artifact?connectionId=$CONNECTION_ID&team=string&folder=string&document=string&timestamp=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "team": "string",
  "folder": "string",
  "document": "string",
  "timestamp": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-timestamp-or-certificate-artifact?${params}`, {
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
| `team` | string | yes | Team UUID from the path. |
| `folder` | string | yes | Folder UUID from the path. |
| `document` | string | yes | Document UUID from the path. |
| `timestamp` | string | yes | Artifact name such as `timestamp.tsr`, `timestamp.asn1`, `timestamp.xml`, or `timestamp.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Timestamp or certificate artifact payload, exposed as a raw string by the current runtime mapping once the document is fully signed. |

## Native endpoint

Through the native CINCEL API, this operation is `GET /teams/:team/folders/:folder/documents/:document/:timestamp` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timestamp-or-certificate-artifact.md) for the provider-specific parameters and requirements.

