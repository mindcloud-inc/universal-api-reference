# Middesk: List policy results for a business

Retrieves policy results for a business in Middesk.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-business-policy-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-business-policy-results?connectionId=$CONNECTION_ID&businessId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "businessId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-business-policy-results?${params}`, {
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
| `businessId` | string | yes | ID of the business whose policy results you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "object": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `object` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /businesses/:business_id/policy_results` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-business-policy-results.md) for the provider-specific parameters and requirements.

