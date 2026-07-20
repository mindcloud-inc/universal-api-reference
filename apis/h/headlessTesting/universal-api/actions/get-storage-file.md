# Headless Testing: Get Storage File

Retrieves a storage file from Headless Testing.

```
GET https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/get-storage-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/get-storage-file?connectionId=$CONNECTION_ID&app_url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "app_url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/get-storage-file?${params}`, {
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
| `app_url` | string | yes | The storage app_url identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app_url": "https://example.com",
      "id": 1,
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app_url` | string |  |
| `id` | number |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Headless Testing API, this operation is `GET /storage/:app_url` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-storage-file.md) for the provider-specific parameters and requirements.

