# 2Smart Cloud: Reference be name



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-share-v1-references-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-share-v1-references-by-name?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/get-share-v1-references-by-name?${params}`, {
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
| `name` | string | yes | Reference name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "is_enabled": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `is_enabled` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /share/v1/references/{name}` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-share-v1-references-by-name.md) for the provider-specific parameters and requirements.

