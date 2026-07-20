# Reportei: Get Company Settings

Retrieves company settings from Reportei.

```
GET https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-company-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-company-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-company-settings?${params}`, {
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
      "company": {
        "id": 1,
        "logo": "string",
        "name": "Ava Chen",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.id` | number | Company identifier |
| `company.logo` | string | Company logo filename |
| `company.name` | string | Company name |
| `company.type` | string | Company type |

## Native endpoint

Through the native Reportei API, this operation is `GET /companies/settings` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-settings.md) for the provider-specific parameters and requirements.

