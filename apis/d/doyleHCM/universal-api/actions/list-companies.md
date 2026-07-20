# Doyle HCM: List companies

Retrieves visible companies from Doyle HCM.

```
GET https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-companies?${params}`, {
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
      "createdOn": "string",
      "fein": "string",
      "id": 1,
      "name": "Ava Chen",
      "status": 1,
      "uiNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | string | Company creation timestamp when available. |
| `fein` | string | Federal employer identification number when returned. |
| `id` | number | Company identifier. |
| `name` | string | Company display name. |
| `status` | number | Company status code. |
| `uiNumber` | number | State unemployment insurance number when returned. |

## Native endpoint

Through the native Doyle HCM API, this operation is `GET /wep/companies` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

