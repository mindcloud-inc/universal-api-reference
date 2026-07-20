# PyPI: Get Project Metadata

Retrieves project metadata and release history from PyPI.

```
GET https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-project-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PyPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-project-metadata?connectionId=$CONNECTION_ID&project=sampleproject" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "sampleproject"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pyPI/latest/actions/get-project-metadata?${params}`, {
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
| `project` | string | yes | The normalized PyPI project name to inspect. Example: `sampleproject`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": {},
      "last_serial": 1,
      "ownership": {},
      "releases": {},
      "urls": [
        {}
      ],
      "vulnerabilities": [
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
| `info` | object | Latest project metadata. |
| `last_serial` | number | Latest serial for the project. |
| `ownership` | object | Project ownership and organization details. |
| `releases` | object | Release map keyed by version. |
| `urls` | array<object> | Distribution files for the latest release. |
| `vulnerabilities` | array<object> | Known vulnerabilities for the latest release. |

## Native endpoint

Through the native PyPI API, this operation is `GET /pypi/:project/json` (base URL `https://pypi.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-metadata.md) for the provider-specific parameters and requirements.

