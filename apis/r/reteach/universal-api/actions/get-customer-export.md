# Reteach: Get Customer Export



```
GET https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reteach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer-export?connectionId=$CONNECTION_ID&customerExportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerExportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer-export?${params}`, {
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
| `customerExportId` | string | yes | The id of the customer export job. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "string",
      "count": 1,
      "failedAt": "string",
      "format": "string",
      "id": "string",
      "includeGroups": true,
      "includeParticipations": true,
      "includeTags": true,
      "size": 1,
      "startedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | string |  |
| `count` | number |  |
| `failedAt` | string |  |
| `format` | string |  |
| `id` | string |  |
| `includeGroups` | boolean |  |
| `includeParticipations` | boolean |  |
| `includeTags` | boolean |  |
| `size` | number |  |
| `startedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Reteach API, this operation is `GET /customer-export/{customerExportId}` (base URL `https://api.reteach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-export.md) for the provider-specific parameters and requirements.

