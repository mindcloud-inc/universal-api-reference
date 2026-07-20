# Doppler Marketing Automation: List Fields

Retrieves fields from Doppler Marketing Automation.

```
GET https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Marketing Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/list-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/list-fields?${params}`, {
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
      "_links": [
        {}
      ],
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | array<object> |  |
| `items` | array<object> |  |

## Native endpoint

Through the native Doppler Marketing Automation API, this operation is `GET /accounts/:accountName/fields` (base URL `https://restapi.fromdoppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

