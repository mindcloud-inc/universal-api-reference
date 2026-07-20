# PageVitals: Get Page Opportunity



```
GET https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page-opportunity?connectionId=$CONNECTION_ID&websiteId=string&pageId=string&opportunityId=string&device=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "pageId": "string",
  "opportunityId": "string",
  "device": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/get-page-opportunity?${params}`, {
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
| `websiteId` | string | yes |  |
| `pageId` | string | yes |  |
| `opportunityId` | string | yes |  |
| `device` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lighthouseVersion": "string",
      "opportunity": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lighthouseVersion` | string |  |
| `opportunity` | object |  |

## Native endpoint

Through the native PageVitals API, this operation is `GET /:websiteId/pages/:pageId/opportunities/:opportunityId` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-opportunity.md) for the provider-specific parameters and requirements.

