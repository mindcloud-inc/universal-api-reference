# Zoho CRM: Get Opportunity Group

Retrieves an Opportunity Group from Zoho CRM.

```
GET https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-opportunity-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-opportunity-group?connectionId=$CONNECTION_ID&opportunityGroupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "opportunityGroupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-opportunity-group?${params}`, {
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
| `opportunityGroupId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Zoho CRM API returns.

## Native endpoint

Through the native Zoho CRM API, this operation is `GET /Opportunity_Groups/:opportunityGroupId` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-opportunity-group.md) for the provider-specific parameters and requirements.

