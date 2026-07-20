# VoilaNorbert: Get Organization

Retrieves current organization details from VoilaNorbert.

```
GET https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoilaNorbert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voilaNorbert/latest/actions/get-organization?${params}`, {
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
      "address": "string",
      "city": "string",
      "company_name": "Ava Chen",
      "country": "string",
      "credits": {},
      "id": 1,
      "is_yearly": true,
      "plan": {},
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `company_name` | string |  |
| `country` | string |  |
| `credits` | object |  |
| `id` | number |  |
| `is_yearly` | boolean |  |
| `plan` | object |  |
| `zipcode` | string |  |

## Native endpoint

Through the native VoilaNorbert API, this operation is `GET /organization/` (base URL `https://api.voilanorbert.com/2018-01-08`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

