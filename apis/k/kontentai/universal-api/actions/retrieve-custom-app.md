# Kontent.ai: Retrieve custom app

Retrieves a custom app from Kontent.ai.

```
GET https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-custom-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kontent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-custom-app?connectionId=$CONNECTION_ID&customAppIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customAppIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kontentai/latest/actions/retrieve-custom-app?${params}`, {
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
| `customAppIdentifier` | string | yes | Kontent.ai custom app identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config_url": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "source_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config_url` | string | Custom app configuration URL. |
| `id` | string | Custom app ID. |
| `name` | string | Custom app name. |
| `source_url` | string | Custom app source URL. |

## Native endpoint

Through the native Kontent.ai API, this operation is `GET https://manage.kontent.ai/v2/projects/:environment_id/custom-apps/:custom_app_identifier` (base URL `https://deliver.kontent.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-custom-app.md) for the provider-specific parameters and requirements.

