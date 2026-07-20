# Optimizely: Get Attribute

Retrieves attribute details from the Optimizely API.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-attribute?connectionId=$CONNECTION_ID&attributeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attributeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-attribute?${params}`, {
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
| `attributeId` | string | yes | The attribute id. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "conditionType": "string",
      "description": "string",
      "id": 1,
      "key": "string",
      "lastModified": "string",
      "name": "Ava Chen",
      "projectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `conditionType` | string |  |
| `description` | string |  |
| `id` | number |  |
| `key` | string |  |
| `lastModified` | string |  |
| `name` | string |  |
| `projectId` | number |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /attributes/{attributeId}` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attribute.md) for the provider-specific parameters and requirements.

