# Google Ads: Generate Ad Group Themes

Generates ad group themes in Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/generate-ad-group-themes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/generate-ad-group-themes?connectionId=$CONNECTION_ID&customerId=1234567890&keywords%5B%5D=string&adGroups%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "keywords[]": "string",
  "adGroups[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/generate-ad-group-themes?${params}`, {
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
| `customerId` | list | yes | Customer ID to generate ad group themes for (without dashes). Example: `1234567890`. |
| `keywords[]` | array<string> | yes | Seed keywords to group into themes. |
| `adGroups[]` | array<string> | yes | Ad group names for thematic grouping. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adGroup": "string",
      "campaign": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adGroup` | string |  |
| `campaign` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId:generateAdGroupThemes` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-ad-group-themes.md) for the provider-specific parameters and requirements.

