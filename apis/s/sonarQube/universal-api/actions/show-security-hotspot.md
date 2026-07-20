# SonarQube: Show Security Hotspot

Retrieves a security hotspot from SonarQube.

```
GET https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/show-security-hotspot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SonarQube `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/show-security-hotspot?connectionId=$CONNECTION_ID&hotspot=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hotspot": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sonarQube/latest/actions/show-security-hotspot?${params}`, {
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
| `hotspot` | string | yes | Security hotspot key. Required by /api/hotspots/show. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "message": "string",
      "project": {},
      "rule": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `message` | string |  |
| `project` | object |  |
| `rule` | object |  |

## Native endpoint

Through the native SonarQube API, this operation is `GET /api/hotspots/show` (base URL `https://sonarcloud.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-security-hotspot.md) for the provider-specific parameters and requirements.

