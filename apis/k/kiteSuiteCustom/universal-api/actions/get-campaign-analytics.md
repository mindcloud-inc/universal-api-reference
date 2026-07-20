# Kite Suite: Get campaign analytics



```
GET https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-campaign-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-campaign-analytics?connectionId=$CONNECTION_ID&campaign=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaign": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/get-campaign-analytics?${params}`, {
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
| `campaign` | string | yes | Campaign ID. |
| `start` | string | no | Start date (YYYY-MM-DD). Defaults to 4 weeks prior. |
| `end` | string | no | End date (YYYY-MM-DD). Defaults to the current date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anylytics": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anylytics` | object |  |

## Native endpoint

Through the native Kite Suite API, this operation is `GET /api/v1/campaign/analytics` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-analytics.md) for the provider-specific parameters and requirements.

