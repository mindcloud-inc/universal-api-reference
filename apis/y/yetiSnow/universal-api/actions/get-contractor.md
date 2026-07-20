# Yeti Snow: Get Contractor



```
GET https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-contractor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yeti Snow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-contractor?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yetiSnow/latest/actions/get-contractor?${params}`, {
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
| `contractorId` | string | no | Contractor identifier from List Contractors. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "code": "string",
      "contacts": [
        {}
      ],
      "contract": {},
      "id": 1,
      "logo": "string",
      "name": "Ava Chen",
      "off_season_mode": "string",
      "uid": "string",
      "user_company": {},
      "weather_works_api_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `code` | string |  |
| `contacts` | array<object> |  |
| `contract` | object |  |
| `id` | number |  |
| `logo` | string |  |
| `name` | string |  |
| `off_season_mode` | string |  |
| `uid` | string |  |
| `user_company` | object |  |
| `weather_works_api_key` | string |  |

## Native endpoint

Through the native Yeti Snow API, this operation is `GET contractor/show/{{contractor_id}}` (base URL `https://sandbox_api.yetisoftware.com/api/en/public_access/1715`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contractor.md) for the provider-specific parameters and requirements.

