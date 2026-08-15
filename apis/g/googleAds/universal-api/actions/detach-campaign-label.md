# Google Ads: Detach Campaign Label

Detaches a label from a campaign in Google Ads.

```
DELETE https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/detach-campaign-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/detach-campaign-label?connectionId=$CONNECTION_ID&customerId=1234567890&operations%5B%5D=%5Bobject%20Object%5D&operations%5B%5D.remove=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "operations[]": "[object Object]",
  "operations[].remove": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/detach-campaign-label?${params}`, {
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
| `customerId` | list | yes | Example: `1234567890`. |
| `operations[]` | array<object> | yes | List of mutate operations. |
| `operations[].remove` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `partialFailure` | boolean | no | Default: `false`. |
| `validateOnly` | boolean | no | Default: `false`. |

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

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/campaignLabels:mutate` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detach-campaign-label.md) for the provider-specific parameters and requirements.

