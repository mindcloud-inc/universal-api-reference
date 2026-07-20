# Numverify: Validate Phone Number

Retrieves validation details for a phone number from Numverify.

```
GET https://connect.mindcloud.co/v1/universal/numverify/latest/actions/validate-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Numverify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/numverify/latest/actions/validate-phone-number?connectionId=$CONNECTION_ID&number=%2B14158586273" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "+14158586273"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/numverify/latest/actions/validate-phone-number?${params}`, {
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
| `number` | string | yes | Phone number to validate. Example: `+14158586273`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `countryCode` | string | no | ISO 3166-1 alpha-2 country code for national-format numbers. Example: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "countryCode": "string",
      "countryName": "Ava Chen",
      "countryPrefix": "string",
      "internationalFormat": "string",
      "lineType": "string",
      "localFormat": "string",
      "location": "string",
      "number": "string",
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `countryCode` | string |  |
| `countryName` | string |  |
| `countryPrefix` | string |  |
| `internationalFormat` | string |  |
| `lineType` | string |  |
| `localFormat` | string |  |
| `location` | string |  |
| `number` | string |  |
| `valid` | boolean |  |

## Native endpoint

Through the native Numverify API, this operation is `GET /validate` (base URL `https://apilayer.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-phone-number.md) for the provider-specific parameters and requirements.

