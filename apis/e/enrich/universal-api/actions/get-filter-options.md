# Enrich.so: Get Filter Options

Retrieves lead filter options from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-filter-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-filter-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-filter-options?${params}`, {
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
      "companySizes": [
        {}
      ],
      "countries": [
        {}
      ],
      "departments": [
        {}
      ],
      "industries": [
        {}
      ],
      "jobFunctions": [
        {}
      ],
      "levels": [
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
| `companySizes` | array<object> | Available company size filter options. |
| `countries` | array<object> | Available country filter options. |
| `departments` | array<object> | Available department filter options. |
| `industries` | array<object> | Available industry filter options. |
| `jobFunctions` | array<object> | Available job function filter options. |
| `levels` | array<object> | Available seniority or level filter options. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /lead-finder/filter-options` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-filter-options.md) for the provider-specific parameters and requirements.

