# Google Ads: Generate Recommendations

Generates recommendations for your Google Ads account.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/generate-recommendations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/generate-recommendations?connectionId=$CONNECTION_ID&customerId=1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/generate-recommendations?${params}`, {
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
| `customerId` | list | yes | Customer ID to generate recommendations for (without dashes). Example: `1234567890`. |
| `recommendationTypes[]` | array<string> | no | Optional recommendation types to generate. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `advertisingChannelType` | string | no | Optional channel type filter for recommendation generation. Example: `SEARCH`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recommendations": [
        {
          "dismissed": true,
          "resourceName": "Ava Chen",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recommendations[].dismissed` | boolean | Whether the generated recommendation is already dismissed. |
| `recommendations[].resourceName` | string | Resource name of a generated recommendation. |
| `recommendations[].type` | string | Type of generated recommendation. |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/recommendations:generate` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-recommendations.md) for the provider-specific parameters and requirements.

