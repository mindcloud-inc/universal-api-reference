# PyPI: Get File Provenance

Retrieves provenance for a PyPI distribution file.

```
GET https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-file-provenance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PyPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-file-provenance?connectionId=$CONNECTION_ID&project=sampleproject&version=4.0.0&filename=sampleproject-4.0.0.tar.gz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "sampleproject",
  "version": "4.0.0",
  "filename": "sampleproject-4.0.0.tar.gz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-file-provenance?${params}`, {
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
| `project` | string | yes | The normalized PyPI project name. Example: `sampleproject`. |
| `version` | string | yes | The release version that owns the uploaded file. Example: `4.0.0`. |
| `filename` | string | yes | The exact distribution filename, including extension. Example: `sampleproject-4.0.0.tar.gz`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attestation_bundles": [
        {}
      ],
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attestation_bundles` | array<object> | Provenance bundles for the requested distribution file. |
| `version` | string | Integrity API version. |

## Native endpoint

Through the native PyPI API, this operation is `GET /integrity/:project/:version/:filename/provenance` (base URL `https://pypi.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-provenance.md) for the provider-specific parameters and requirements.

