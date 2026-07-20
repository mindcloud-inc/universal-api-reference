# Kontent.ai: Upsert management asset

Upserts an asset in Kontent.ai by external ID.

```
PUT https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/upsert-management-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/upsert-management-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "externalId": "string",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/upsert-management-asset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "externalId": "string",
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | yes | External ID used to upsert the Kontent.ai asset. |
| `body` | object | yes | JSON request body for upserting a Kontent.ai management asset. |

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
| `title` | string | Asset title. |
| `url` | string | Asset URL. |

## Native endpoint

Through the native Kontent.ai API, this operation is `PUT https://manage.kontent.ai/v2/projects/:environment_id/assets/external-id/:external_id` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-management-asset.md) for the provider-specific parameters and requirements.

