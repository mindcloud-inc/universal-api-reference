# Planday: Get Portal Information

Retrieves basic portal details from Planday.

```
GET https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-portal-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-portal-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-portal-information?${params}`, {
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
      "aliases": [
        "string"
      ],
      "companyName": "Ava Chen",
      "country": "string",
      "id": 1,
      "maxDepartments": 1,
      "name": "Ava Chen",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aliases` | array<string> |  |
| `companyName` | string |  |
| `country` | string |  |
| `id` | number |  |
| `maxDepartments` | number |  |
| `name` | string |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Planday API, this operation is `GET /portal/v1.0/info` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-portal-information.md) for the provider-specific parameters and requirements.

