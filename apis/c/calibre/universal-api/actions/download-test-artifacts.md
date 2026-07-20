# Calibre: Download Test Artifacts

Retrieves artifact download URLs for a page test from Calibre.

```
GET https://connect.mindcloud.co/v1/universal/calibre/latest/actions/download-test-artifacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/download-test-artifacts?connectionId=$CONNECTION_ID&variables.uuid=string&variables.artifactName=TEST_ARTIFACT_LIGHTHOUSE&variables.mediaName=TEST_MEDIA_IMAGE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.uuid": "string",
  "variables.artifactName": "TEST_ARTIFACT_LIGHTHOUSE",
  "variables.mediaName": "TEST_MEDIA_IMAGE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/download-test-artifacts?${params}`, {
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
| `variables.uuid` | string | yes |  |
| `variables.artifactName` | string | yes | Default: `TEST_ARTIFACT_LIGHTHOUSE`. |
| `variables.mediaName` | string | yes | Default: `TEST_MEDIA_IMAGE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organisation": {
        "singlePageTest": {
          "artifactURL": "https://example.com",
          "mediaURL": "https://example.com",
          "uuid": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organisation.singlePageTest.artifactURL` | string |  |
| `organisation.singlePageTest.mediaURL` | string |  |
| `organisation.singlePageTest.uuid` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-test-artifacts.md) for the provider-specific parameters and requirements.

