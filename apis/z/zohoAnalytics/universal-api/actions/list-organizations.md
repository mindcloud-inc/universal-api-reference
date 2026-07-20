# Zoho Analytics: List Organizations

Retrieves available organizations from Zoho Analytics.

```
GET https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/list-organizations?${params}`, {
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
        "orgs": [
          {
            "createdBy": "string",
            "createdByZuId": "string",
            "isDefault": true,
            "numberOfWorkspaces": 1,
            "orgDesc": "string",
            "orgId": "string",
            "orgName": "Ava Chen",
            "planName": "Ava Chen",
            "role": "string"
          }
        ]
      },
      "status": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.orgs[].createdBy` | string |  |
| `data.orgs[].createdByZuId` | string |  |
| `data.orgs[].isDefault` | boolean |  |
| `data.orgs[].numberOfWorkspaces` | number |  |
| `data.orgs[].orgDesc` | string |  |
| `data.orgs[].orgId` | string |  |
| `data.orgs[].orgName` | string |  |
| `data.orgs[].planName` | string |  |
| `data.orgs[].role` | string |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `GET /orgs` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

