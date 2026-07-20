# Dealfront: Get Feed Export Status

Retrieves feed export status from Dealfront.

```
GET https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/get-feed-export-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dealfront `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/get-feed-export-status?connectionId=$CONNECTION_ID&exportRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exportRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/get-feed-export-status?${params}`, {
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
| `exportRequestId` | string | yes | ID of the export request to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "string",
        "downloadUrl": "https://example.com",
        "status": "string",
        "statusUrl": "https://example.com"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | string |  |
| `attributes.downloadUrl` | string |  |
| `attributes.status` | string |  |
| `attributes.statusUrl` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dealfront API, this operation is `GET /export-requests/:id` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feed-export-status.md) for the provider-specific parameters and requirements.

