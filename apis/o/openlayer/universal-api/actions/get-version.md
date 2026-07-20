# Openlayer: Get Version

Retrieves version details from the Openlayer API.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-version?connectionId=$CONNECTION_ID&versionId=67ef0916-c639-4a06-9309-62e906234bb7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "versionId": "67ef0916-c639-4a06-9309-62e906234bb7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-version?${params}`, {
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
| `versionId` | string | yes | The project version ID. Default: `67ef0916-c639-4a06-9309-62e906234bb7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commit": {
        "id": "string",
        "message": "string",
        "source": "string"
      },
      "dateCreated": "string",
      "deploymentStatus": "string",
      "failingGoalCount": 1,
      "id": "string",
      "links": {
        "app": "https://example.com"
      },
      "passingGoalCount": 1,
      "projectId": "string",
      "status": "string",
      "totalGoalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commit.id` | string |  |
| `commit.message` | string |  |
| `commit.source` | string |  |
| `dateCreated` | string |  |
| `deploymentStatus` | string |  |
| `failingGoalCount` | number |  |
| `id` | string |  |
| `links.app` | string |  |
| `passingGoalCount` | number |  |
| `projectId` | string |  |
| `status` | string |  |
| `totalGoalCount` | number |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /versions/:versionId` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-version.md) for the provider-specific parameters and requirements.

