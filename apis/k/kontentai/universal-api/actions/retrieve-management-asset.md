# Kontent.ai: Retrieve management asset

Retrieves an asset from your Kontent.ai environment.

```
GET https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-management-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-management-asset?connectionId=$CONNECTION_ID&assetIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-management-asset?${params}`, {
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
| `assetIdentifier` | string | yes | Kontent.ai asset identifier, such as the asset codename or ID accepted by the Management API. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "external_id": "string",
      "file_name": "Ava Chen",
      "id": "string",
      "last_modified": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Asset description. |
| `external_id` | string | Asset external ID. |
| `file_name` | string | Asset file name. |
| `id` | string | Asset ID. |
| `last_modified` | date | Last modified timestamp. |
| `title` | string | Asset title. |
| `url` | string | Asset URL. |

## Native endpoint

Through the native Kontent.ai API, this operation is `GET https://manage.kontent.ai/v2/projects/:environment_id/assets/:asset_identifier` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-management-asset.md) for the provider-specific parameters and requirements.

