# urlscan.io: Reset Result Visibility

Deletes a scan result visibility override in urlscan.io.

```
DELETE https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/reset-result-visibility
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a urlscan.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/reset-result-visibility?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/urlscanio/latest/actions/reset-result-visibility?${params}`, {
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
| `scanId` | string | no | The scan UUID whose visibility you want to reset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "uuid": "string"
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

## Native endpoint

Through the native urlscan.io API, this operation is `DELETE /api/v1/result/{scanId}/visibility/` (base URL `https://urlscan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reset-result-visibility.md) for the provider-specific parameters and requirements.

