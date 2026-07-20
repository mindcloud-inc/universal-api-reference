# Interzoid: Get Business Info



```
GET https://connect.mindcloud.co/v1/universal/interzoid/latest/actions/get-business-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Interzoid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/interzoid/latest/actions/get-business-info?connectionId=$CONNECTION_ID&lookup=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lookup": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/interzoid/latest/actions/get-business-info?${params}`, {
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
| `lookup` | string | yes | Company name, web domain, or email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": "string",
      "CompanyDescription": "string",
      "CompanyLocation": "string",
      "CompanyName": "Ava Chen",
      "CompanyURL": "https://example.com",
      "Credits": "string",
      "NAICS": "string",
      "NumberEmployees": "string",
      "Revenue": "string",
      "TopExecutive": "string",
      "TopExecutiveTitle": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string |  |
| `CompanyDescription` | string |  |
| `CompanyLocation` | string |  |
| `CompanyName` | string |  |
| `CompanyURL` | string |  |
| `Credits` | string |  |
| `NAICS` | string |  |
| `NumberEmployees` | string |  |
| `Revenue` | string |  |
| `TopExecutive` | string |  |
| `TopExecutiveTitle` | string |  |

## Native endpoint

Through the native Interzoid API, this operation is `GET /getbusinessinfo` (base URL `https://api.interzoid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-business-info.md) for the provider-specific parameters and requirements.

