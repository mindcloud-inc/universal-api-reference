# The Org: Get Current Usage

Retrieves current API usage from The Org.

```
GET https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/get-current-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a The Org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/get-current-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/theOrg/latest/actions/get-current-usage?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "additionalCredits": 1,
        "creditOverages": 1,
        "planCredits": 1,
        "planInterval": "string",
        "planResetDate": "string",
        "unlimited": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.additionalCredits` | number | Additional purchased credits |
| `data.creditOverages` | number | Current credit overages |
| `data.planCredits` | number | Included plan credits |
| `data.planInterval` | string | Billing interval for the current plan |
| `data.planResetDate` | string | Billing period reset date returned by The Org |
| `data.unlimited` | boolean | Whether the plan is unlimited |

## Native endpoint

Through the native The Org API, this operation is `GET /v1.1/usage` (base URL `https://api.theorg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-usage.md) for the provider-specific parameters and requirements.

