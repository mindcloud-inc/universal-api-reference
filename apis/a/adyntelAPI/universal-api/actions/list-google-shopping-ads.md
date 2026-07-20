# Adyntel: List Google Shopping Ads

Starts a Google Shopping ad search in Adyntel by company domain.

```
GET https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/list-google-shopping-ads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adyntel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/list-google-shopping-ads?connectionId=$CONNECTION_ID&companyDomain=shopify.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyDomain": "shopify.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/list-google-shopping-ads?${params}`, {
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
| `companyDomain` | string | yes | Company website. Example: `shopify.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Adyntel API, this operation is `POST /google_shopping` (base URL `https://api.adyntel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-google-shopping-ads.md) for the provider-specific parameters and requirements.

