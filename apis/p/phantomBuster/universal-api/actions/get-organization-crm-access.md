# PhantomBuster: Get Organization CRM Access

Retrieves organization CRM access from PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-organization-crm-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-organization-crm-access?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-organization-crm-access?${params}`, {
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
      "accessToken": "string",
      "contactUpdateOnly": true,
      "crmAccountId": "string",
      "crmName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `contactUpdateOnly` | boolean |  |
| `crmAccountId` | string |  |
| `crmName` | string |  |

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /orgs/fetch-crm-access` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-crm-access.md) for the provider-specific parameters and requirements.

