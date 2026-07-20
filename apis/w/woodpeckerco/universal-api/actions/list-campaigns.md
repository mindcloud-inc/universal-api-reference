# Woodpecker.co: List Campaigns

Retrieves campaigns from Woodpecker, optionally filtered by status.

```
GET https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woodpecker.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/woodpeckerco/latest/actions/list-campaigns?${params}`, {
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
| `status` | string | no | Optional Woodpecker campaign status filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bcc": "string",
      "cc": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "error": "string",
      "folderId": 1,
      "folderName": "Ava Chen",
      "fromEmail": "ava@example.com",
      "fromName": "Ava Chen",
      "gdprUnsubscribe": true,
      "id": 1,
      "name": "Ava Chen",
      "perDay": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bcc` | string |  |
| `cc` | string |  |
| `created` | date |  |
| `error` | string |  |
| `folderId` | number |  |
| `folderName` | string |  |
| `fromEmail` | string |  |
| `fromName` | string |  |
| `gdprUnsubscribe` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `perDay` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Woodpecker.co API, this operation is `GET /rest/v1/campaign_list` (base URL `https://api.woodpecker.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

