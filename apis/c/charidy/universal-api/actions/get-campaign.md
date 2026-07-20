# Charidy: Get Campaign

Retrieves a campaign from Charidy.

```
GET https://connect.mindcloud.co/v1/universal/charidy/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Charidy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/charidy/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=96" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "96"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/charidy/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | number | yes | The campaign ID to retrieve. Example: `96`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "campaignId": 1,
        "campaignImage": "string",
        "category": "string",
        "currency": "string",
        "currencySign": "string",
        "endDate": "2026-05-07T12:00:00.000Z",
        "mode": 1,
        "shortDescription": "string",
        "shortLink": "https://example.com",
        "startDate": "2026-05-07T12:00:00.000Z",
        "theme": "string",
        "title": "string"
      },
      "id": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.campaignId` | number | Campaign ID. |
| `attributes.campaignImage` | string | Primary campaign image URL. |
| `attributes.category` | string | Campaign category. |
| `attributes.currency` | string | Campaign currency code. |
| `attributes.currencySign` | string | Campaign currency sign. |
| `attributes.endDate` | date | Campaign end date. |
| `attributes.mode` | number | Campaign mode code. |
| `attributes.shortDescription` | string | Campaign short description. |
| `attributes.shortLink` | string | Campaign short link. |
| `attributes.startDate` | date | Campaign start date. |
| `attributes.theme` | string | Campaign theme. |
| `attributes.title` | string | Campaign title. |
| `id` | number | Unique campaign ID. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Charidy API, this operation is `GET /api/v1/campaign/:campaignId` (base URL `https://api.charidy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

