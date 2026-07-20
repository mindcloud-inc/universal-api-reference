# urlscan.io: Update Result Visibility

Updates a scan result's visibility in urlscan.io.

```
PUT https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/update-result-visibility
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a urlscan.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/update-result-visibility" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/update-result-visibility', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scanId` | string | no | The scan UUID whose visibility you want to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "uuid": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `uuid` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native urlscan.io API, this operation is `PUT /api/v1/result/{scanId}/visibility/` (base URL `https://urlscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-result-visibility.md) for the provider-specific parameters and requirements.

