# LinkedIn Ads Reports: Get Ad Account

Retrieves an ad account from LinkedIn Ads Reports.

```
GET https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-ad-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn Ads Reports `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-ad-account?connectionId=$CONNECTION_ID&adAccountId=123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "adAccountId": "123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-ad-account?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "id": "string",
      "name": "Ava Chen",
      "reference": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `id` | string |  |
| `name` | string |  |
| `reference` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native LinkedIn Ads Reports API, this operation is `GET /rest/adAccounts/{{adAccountId}}` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ad-account.md) for the provider-specific parameters and requirements.

