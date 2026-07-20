# Ziflow: List Integrations

Retrieves integrations from your Ziflow account.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-integrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-integrations?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "application_key": "string",
      "description": "string",
      "name": "Ava Chen",
      "settings": {
        "integration_properties_enabled": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application_key` | string |  |
| `description` | string |  |
| `name` | string |  |
| `settings.integration_properties_enabled` | string |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /integrations` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-integrations.md) for the provider-specific parameters and requirements.

