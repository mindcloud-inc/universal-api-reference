# Contentful: Get asset



```
GET https://connect.mindcloud.co/v1/universal/contentful/latest/actions/get-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contentful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentful/latest/actions/get-asset?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentful/latest/actions/get-asset?${params}`, {
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
| `assetId` | string | no |  |
| `environmentId` | string | no |  |
| `spaceId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sys": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "type": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "version": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sys.createdAt` | date |  |
| `sys.id` | string |  |
| `sys.type` | string |  |
| `sys.updatedAt` | date |  |
| `sys.version` | number |  |

## Native endpoint

Through the native Contentful API, this operation is `GET /spaces/:spaceId/environments/:environmentId/assets/:assetId` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset.md) for the provider-specific parameters and requirements.

