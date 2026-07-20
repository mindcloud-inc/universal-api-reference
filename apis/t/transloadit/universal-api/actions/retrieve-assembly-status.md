# Transloadit: Retrieve Assembly Status

Retrieves an assembly status from Transloadit.

```
GET https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-assembly-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-assembly-status?connectionId=$CONNECTION_ID&assemblyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assemblyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/retrieve-assembly-status?${params}`, {
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
| `assemblyId` | string | yes | The ID of the assembly to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assembly_id": "string",
      "assembly_ssl_url": "https://example.com",
      "message": "string",
      "ok": "string",
      "params": "string",
      "results": {},
      "uploads": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assembly_id` | string | Assembly ID. |
| `assembly_ssl_url` | string | Secure URL of the assembly. |
| `message` | string | Human-readable result message. |
| `ok` | string | Status code returned by Transloadit for assembly retrieval. |
| `params` | string | Original assembly instructions JSON string. |
| `results` | object | Assembly results grouped by step. |
| `uploads` | array<object> | Uploads attached to the assembly. |

## Native endpoint

Through the native Transloadit API, this operation is `GET /assemblies/:assemblyId` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-assembly-status.md) for the provider-specific parameters and requirements.

