# Localazy: List CDN Metadata

Retrieves CDN metadata from a Localazy project.

```
GET https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-cdn-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-cdn-metadata?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-cdn-metadata?${params}`, {
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
| `projectId` | string | yes | Localazy project identifier or slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enabled": true,
      "metadataUrls": [
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
| `enabled` | boolean | Whether CDN metadata delivery is enabled for the project. |
| `metadataUrls` | array<object> | Metadata file URLs for published CDN release tags. |

## Native endpoint

Through the native Localazy API, this operation is `GET /projects/:projectId/cdn` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cdn-metadata.md) for the provider-specific parameters and requirements.

