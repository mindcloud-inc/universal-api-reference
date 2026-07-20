# Dealfront: Request Feed Export

Creates a new feed export request in Dealfront.

```
POST https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/request-feed-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dealfront `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/request-feed-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "customFeedId": "string",
  "startDate": "string",
  "endDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dealfront/latest/actions/request-feed-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "customFeedId": "string",
    "startDate": "string",
    "endDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | ID of the account you want to export leads from. |
| `customFeedId` | string | yes | ID of the custom feed to export. Use all_leads to export all leads. |
| `startDate` | string | yes | Start date for the export window in YYYY-MM-DD format. |
| `endDate` | string | yes | End date for the export window in YYYY-MM-DD format. |

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

Through the native Dealfront API, this operation is `POST /export-requests` (base URL `https://api.leadfeeder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-feed-export.md) for the provider-specific parameters and requirements.

