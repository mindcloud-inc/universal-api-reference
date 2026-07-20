# 7shifts: Retrieve Labor Settings

Retrieves company labor settings from 7shifts.

```
GET https://connect.mindcloud.co/v1/universal/shifts/latest/actions/retrieve-labor-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 7shifts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/retrieve-labor-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shifts/latest/actions/retrieve-labor-settings?${params}`, {
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
      "company_id": 1,
      "settings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | number |  |
| `settings` | object |  |

## Native endpoint

Through the native 7shifts API, this operation is `GET /v2/company/{company_id}/labor_settings` (base URL `https://api.7shifts.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-labor-settings.md) for the provider-specific parameters and requirements.

