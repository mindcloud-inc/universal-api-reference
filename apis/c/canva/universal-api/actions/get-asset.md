# Canva: Get Asset

Retrieves details for a Canva asset.

```
GET https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-asset?connectionId=$CONNECTION_ID&assetId=MAHDrno82A8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetId": "MAHDrno82A8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-asset?${params}`, {
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
| `assetId` | string | yes | The ID of the asset. Example: `MAHDrno82A8`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asset": {
        "createdAt": 1,
        "id": "string",
        "importStatus": {
          "state": "string"
        },
        "metadata": {
          "height": 1,
          "smartTags": [
            "string"
          ],
          "type": "string",
          "width": 1
        },
        "name": "Ava Chen",
        "owner": {
          "teamId": "string",
          "userId": "string"
        },
        "tags": [
          "string"
        ],
        "thumbnail": {
          "height": 1,
          "url": "https://example.com",
          "width": 1
        },
        "type": "string",
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asset` | object |  |
| `asset.createdAt` | number |  |
| `asset.id` | string |  |
| `asset.importStatus` | object |  |
| `asset.importStatus.state` | string |  |
| `asset.metadata` | object |  |
| `asset.metadata.height` | number |  |
| `asset.metadata.smartTags` | array<string> |  |
| `asset.metadata.type` | string |  |
| `asset.metadata.width` | number |  |
| `asset.name` | string |  |
| `asset.owner` | object |  |
| `asset.owner.teamId` | string |  |
| `asset.owner.userId` | string |  |
| `asset.tags` | array<string> |  |
| `asset.thumbnail` | object |  |
| `asset.thumbnail.height` | number |  |
| `asset.thumbnail.url` | string |  |
| `asset.thumbnail.width` | number |  |
| `asset.type` | string |  |
| `asset.updatedAt` | number |  |

## Native endpoint

Through the native Canva API, this operation is `GET /v1/assets/:assetId` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset.md) for the provider-specific parameters and requirements.

