# Campaign Cleaner: Get Campaign

Retrieves a campaign from Campaign Cleaner.

```
GET https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Cleaner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaign.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaign.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/get-campaign?${params}`, {
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
| `campaign.id` | string | yes | The campaign ID to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaign.minimize_html` | boolean | no | When enabled, removes extra whitespace from the returned campaign HTML to reduce payload size. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {},
      "error": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object | Full processed campaign payload including settings, campaign_html, deliverability metrics, and summary arrays. |
| `error` | string | Provider-level error message when the campaign could not be returned. |

## Native endpoint

Through the native Campaign Cleaner API, this operation is `POST /v1/get_campaign` (base URL `https://api.campaigncleaner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

