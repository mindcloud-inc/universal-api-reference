# Campaign Cleaner: Get Campaign PDF Analysis

Retrieves a campaign PDF analysis from Campaign Cleaner.

```
GET https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/get-campaign-pdf-analysis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Cleaner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/get-campaign-pdf-analysis?connectionId=$CONNECTION_ID&campaign.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaign.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignCleaner/latest/actions/get-campaign-pdf-analysis?${params}`, {
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
| `campaign.id` | string | yes | The campaign ID to export as PDF. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Binary PDF bytes returned by the API as an array of numbers. |
| `type` | string | Node Buffer marker for the binary PDF payload. |

## Native endpoint

Through the native Campaign Cleaner API, this operation is `POST /v1/get_campaign_pdf_analysis` (base URL `https://api.campaigncleaner.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-pdf-analysis.md) for the provider-specific parameters and requirements.

