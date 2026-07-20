# BigDataCloud: Validate Phone Number by IP

Validates a phone number by IP address in BigDataCloud.

```
GET https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/validate-phone-number-by-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigDataCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/validate-phone-number-by-ip?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigDataCloud/latest/actions/validate-phone-number-by-ip?${params}`, {
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
| `number` | string | no | Phone number to validate. Example: `884633490`. |
| `ip` | string | no | IPv4 or IPv6 address. If omitted, the caller IP address is assumed. Example: `193.114.112.1`. |
| `localityLanguage` | string | no | Preferred language for locality names in ISO 639-1 format. Default: `en`. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": {},
      "e164Format": "string",
      "internationalFormat": "string",
      "isValid": true,
      "lineType": "string",
      "location": "string",
      "nationalFormat": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | object | Country details for the validated phone number. |
| `e164Format` | string | The number formatted in E164 standard format. |
| `internationalFormat` | string | The number formatted in international dial format. |
| `isValid` | boolean | Indicates whether the number is valid. |
| `lineType` | string | Detected line type. |
| `location` | string | Estimated location localized to the requested locality language. |
| `nationalFormat` | string | The number formatted in local dial format. |

## Native endpoint

Through the native BigDataCloud API, this operation is `GET /data/phone-number-validate-by-ip` (base URL `https://api-bdc.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-phone-number-by-ip.md) for the provider-specific parameters and requirements.

