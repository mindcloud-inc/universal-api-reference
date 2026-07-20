# PyPI: Get Project Files Index

Retrieves distribution download URLs for a PyPI project.

```
GET https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-project-files-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PyPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-project-files-index?connectionId=$CONNECTION_ID&project=sampleproject" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "sampleproject"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-project-files-index?${params}`, {
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
| `project` | string | yes | The normalized PyPI project name whose file index you want to list. Example: `sampleproject`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alternate-locations": [
        "string"
      ],
      "files": [
        {}
      ],
      "meta": {},
      "name": "Ava Chen",
      "project-status": {},
      "versions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternate-locations` | array<string> | Alternate locations for the project index when present. |
| `files` | array<object> | Distribution files published for the project. |
| `meta` | object | Index metadata including API version and serial. |
| `name` | string | Normalized project name. |
| `project-status` | object | Project status flags returned by the simple API. |
| `versions` | array<string> | Versions known to the simple API. |

## Native endpoint

Through the native PyPI API, this operation is `GET /simple/:project/` (base URL `https://pypi.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-files-index.md) for the provider-specific parameters and requirements.

