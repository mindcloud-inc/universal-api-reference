# Novofon: List Direct Number Countries

Retrieves direct number countries from Novofon.

```
GET https://connect.mindcloud.co/v1/universal/novofon/latest/actions/list-direct-number-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Novofon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/novofon/latest/actions/list-direct-number-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/novofon/latest/actions/list-direct-number-countries?${params}`, {
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
| `language` | string | no | Optional response language. If omitted, Novofon uses the account language. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": [
        {
          "countryCode": "string",
          "countryCodeIso": "string",
          "name": "Ava Chen"
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `info[].countryCode` | string |  |
| `info[].countryCodeIso` | string |  |
| `info[].name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Novofon API, this operation is `GET /v1/direct_numbers/countries/` (base URL `https://api.novofon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-direct-number-countries.md) for the provider-specific parameters and requirements.

