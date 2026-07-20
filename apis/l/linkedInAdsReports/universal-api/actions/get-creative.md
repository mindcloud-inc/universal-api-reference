# LinkedIn Ads Reports: Get Creative

Retrieves a creative from LinkedIn Ads Reports.

```
GET https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-creative
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn Ads Reports `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-creative?connectionId=$CONNECTION_ID&adAccountId=123456&creativeId=urn%253Ali%253AsponsoredCreative%253A123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adAccountId": "123456",
  "creativeId": "urn%3Ali%3AsponsoredCreative%3A123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-creative?${params}`, {
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
| `adAccountId` | string | yes | LinkedIn numeric ad account ID. Default: `123456`. |
| `creativeId` | string | yes | LinkedIn numeric creative ID. Default: `urn%3Ali%3AsponsoredCreative%3A123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "campaign": "string",
      "content": {},
      "createdAt": 1,
      "id": "string",
      "lastModifiedAt": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `campaign` | string |  |
| `content` | object |  |
| `createdAt` | number |  |
| `id` | string |  |
| `lastModifiedAt` | number |  |
| `status` | string |  |

## Native endpoint

Through the native LinkedIn Ads Reports API, this operation is `GET /rest/adAccounts/{{adAccountId}}/creatives/{{creativeId}}` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-creative.md) for the provider-specific parameters and requirements.

