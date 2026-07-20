# Cloudmersive: Parse Address String

Parses an address string in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/parse-address-string
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/parse-address-string?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/parse-address-string?${params}`, {
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
| `AddressString` | string | no | Unstructured address string to parse. |
| `CapitalizationMode` | string | no | Optional capitalization mode for the parsed address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "building": "string",
      "city": "string",
      "countryFullName": "Ava Chen",
      "isoTwoLetterCode": "string",
      "postalCode": "string",
      "stateOrProvince": "string",
      "street": "string",
      "streetNumber": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `building` | string |  |
| `city` | string |  |
| `countryFullName` | string |  |
| `isoTwoLetterCode` | string |  |
| `postalCode` | string |  |
| `stateOrProvince` | string |  |
| `street` | string |  |
| `streetNumber` | string |  |
| `successful` | boolean |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/address/parse` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-address-string.md) for the provider-specific parameters and requirements.

