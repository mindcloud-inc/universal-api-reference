# Google Ads: Create Responsive Search Ad

Creates a responsive search ad in Google Ads.

```
POST https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-responsive-search-ad
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-responsive-search-ad" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "1234567890",
  "operations[]": [
    {}
  ],
  "operations[].create.adGroup": "customers/1234567890/adGroups/9876543210",
  "operations[].create.ad.finalUrls[]": "https://www.example.com",
  "operations[].create.ad.responsiveSearchAd.headlines[]": [
    {}
  ],
  "operations[].create.ad.responsiveSearchAd.descriptions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/create-responsive-search-ad', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "1234567890",
    "operations[]": [{}],
    "operations[].create.adGroup": "customers/1234567890/adGroups/9876543210",
    "operations[].create.ad.finalUrls[]": "https://www.example.com",
    "operations[].create.ad.responsiveSearchAd.headlines[]": [{}],
    "operations[].create.ad.responsiveSearchAd.descriptions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | list | yes | Example: `1234567890`. |
| `operations[]` | array<object> | yes | Mutate operations to apply for ad group ads. |
| `operations[].create` | object | no | Ad group ad creation payload. |
| `operations[].create.ad` | object | no | Ad content payload. |
| `operations[].create.ad.responsiveSearchAd` | object | no | Responsive search ad fields. |
| `operations[].create.status` | list | no | One of: `ENABLED`, `PAUSED`, `REMOVED`, `UNKNOWN`, `UNSPECIFIED`. Default: `PAUSED`. |
| `operations[].create.adGroup` | string | yes | Example: `customers/1234567890/adGroups/9876543210`. |
| `operations[].create.ad.finalUrls[]` | array<string> | yes | Example: `https://www.example.com`. |
| `operations[].create.ad.responsiveSearchAd.headlines[]` | array<object> | yes | Headline assets for the responsive search ad (array of objects with text). |
| `operations[].create.ad.responsiveSearchAd.descriptions[]` | array<object> | yes | Description assets for the responsive search ad (array of objects with text). |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `partialFailure` | boolean | no | Default: `false`. |
| `validateOnly` | boolean | no | Default: `true`. |
| `responseContentType` | list | no | One of: `MUTABLE_RESOURCE`, `RESOURCE_NAME_ONLY`, `UNSPECIFIED`. Default: `RESOURCE_NAME_ONLY`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resourceName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resourceName` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/adGroupAds:mutate` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-responsive-search-ad.md) for the provider-specific parameters and requirements.

