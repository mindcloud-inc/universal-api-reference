# Google Ads: Attach Keyword Label

Attaches a label to a keyword criterion in Google Ads.

```
POST https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/attach-keyword-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/attach-keyword-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "1234567890",
  "operations[]": [
    {}
  ],
  "operations[].create.adGroupCriterion": "string",
  "operations[].create.label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/attach-keyword-label', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "1234567890",
    "operations[]": [{}],
    "operations[].create.adGroupCriterion": "string",
    "operations[].create.label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | list | yes | Example: `1234567890`. |
| `operations[]` | array<object> | yes | List of mutate operations. |
| `operations[].create` | object | no | Create payload for each mutate operation. |
| `operations[].create.adGroupCriterion` | string | yes |  |
| `operations[].create.label` | string | yes |  |

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

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/adGroupCriterionLabels:mutate` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-keyword-label.md) for the provider-specific parameters and requirements.

