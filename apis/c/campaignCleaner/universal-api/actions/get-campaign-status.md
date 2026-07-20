# Campaign Cleaner: Get Campaign Status

Retrieves a campaign's status from Campaign Cleaner.

```
GET https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/get-campaign-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Cleaner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/get-campaign-status?connectionId=$CONNECTION_ID&campaign.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaign.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/get-campaign-status?${params}`, {
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
| `campaign.id` | string | yes | The campaign ID to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignStatus": {},
      "error": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignStatus` | object | Campaign status payload including id, campaign_name, status, and date_added. |
| `error` | string | Provider-level error message when the campaign could not be resolved. |

## Native endpoint

Through the native Campaign Cleaner API, this operation is `POST /v1/get_campaign_status` (base URL `https://api.campaigncleaner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-status.md) for the provider-specific parameters and requirements.

