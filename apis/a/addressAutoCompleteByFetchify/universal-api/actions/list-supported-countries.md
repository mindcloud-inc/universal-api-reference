# Address Auto-Complete by Fetchify: List Supported Countries

Retrieves supported address countries from Fetchify.

```
GET https://connect.mindcloud.co/v1/universal/addressAutoCompleteByFetchify/latest/actions/list-supported-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Address Auto-Complete by Fetchify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressAutoCompleteByFetchify/latest/actions/list-supported-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressAutoCompleteByFetchify/latest/actions/list-supported-countries?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | no | Optional response language for country names. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countries": [
        {
          "code": "string",
          "countryName": "Ava Chen",
          "intlLongName": "Ava Chen",
          "iso31661Alpha2": "string",
          "iso31661Alpha3": "string",
          "iso31661Numeric3": 1,
          "officialName": "Ava Chen",
          "shortCode": "string"
        }
      ],
      "ipLocation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countries[].code` | string |  |
| `countries[].countryName` | string |  |
| `countries[].intlLongName` | string |  |
| `countries[].iso31661Alpha2` | string |  |
| `countries[].iso31661Alpha3` | string |  |
| `countries[].iso31661Numeric3` | number |  |
| `countries[].officialName` | string |  |
| `countries[].shortCode` | string |  |
| `ipLocation` | string |  |

## Native endpoint

Through the native Address Auto-Complete by Fetchify API, this operation is `GET /countries` (base URL `https://api.craftyclicks.co.uk/address/1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-countries.md) for the provider-specific parameters and requirements.

