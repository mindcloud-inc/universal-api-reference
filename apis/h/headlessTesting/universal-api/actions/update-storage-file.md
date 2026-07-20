# Headless Testing: Update Storage File

Updates a storage file in Headless Testing.

```
PUT https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-storage-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-storage-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "app_url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/update-storage-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "app_url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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

Through the native Headless Testing API, this operation is `POST /storage/:app_url` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-storage-file.md) for the provider-specific parameters and requirements.

