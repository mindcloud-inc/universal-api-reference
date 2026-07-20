# Campaign Cleaner: Delete Campaign

Deletes a campaign from Campaign Cleaner.

```
DELETE https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/delete-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Cleaner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/delete-campaign?connectionId=$CONNECTION_ID&campaign.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaign.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/delete-campaign?${params}`, {
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
| `campaign.id` | string | yes | The campaign ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Provider-level error message when the campaign could not be deleted. |
| `status` | string | Deletion result status when the provider returns an explicit status. |

## Native endpoint

Through the native Campaign Cleaner API, this operation is `POST /v1/delete_campaign` (base URL `https://api.campaigncleaner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-campaign.md) for the provider-specific parameters and requirements.

