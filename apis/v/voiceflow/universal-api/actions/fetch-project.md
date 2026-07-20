# Voiceflow: Fetch Project

Retrieves exported project files from Voiceflow.

```
GET https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/fetch-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/fetch-project?connectionId=$CONNECTION_ID&versionId=development" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "versionId": "development"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/fetch-project?${params}`, {
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
| `versionId` | string | yes | Voiceflow project version ID, or the alias development or production when used with the projectID header. Example: `development`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prototype` | string | no | Return the concise .vfr export when true. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_version": "string",
      "diagrams": {},
      "flows": [
        {}
      ],
      "project": {
        "_id": "string",
        "devVersion": "string",
        "liveVersion": "string",
        "name": "Ava Chen",
        "platform": "string"
      },
      "transcriptEvaluations": [
        {}
      ],
      "variables": [
        {}
      ],
      "version": {
        "_id": "string",
        "name": "Ava Chen",
        "projectID": "string",
        "rootDiagramID": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_version` | string | Export format version. |
| `diagrams` | object | Project diagram definitions keyed by diagram ID. |
| `flows` | array<object> | Flow definitions included in the export. |
| `project._id` | string | Project ID. |
| `project.devVersion` | string | Development version ID. |
| `project.liveVersion` | string | Published version ID. |
| `project.name` | string | Project name. |
| `project.platform` | string | Primary project platform. |
| `transcriptEvaluations` | array<object> | Transcript evaluations included in the export. |
| `variables` | array<object> | Version variables included in the export. |
| `version._id` | string | Fetched version ID. |
| `version.name` | string | Fetched version name. |
| `version.projectID` | string | Owning project ID for the version. |
| `version.rootDiagramID` | string | Root diagram ID for the version. |

## Native endpoint

Through the native Voiceflow API, this operation is `GET https://api.voiceflow.com/v2/versions/:versionId/export` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-project.md) for the provider-specific parameters and requirements.

