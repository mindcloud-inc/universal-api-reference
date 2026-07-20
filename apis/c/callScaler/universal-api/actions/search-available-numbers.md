# CallScaler: Search Available Numbers

Finds available numbers in CallScaler.

```
GET https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/search-available-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallScaler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/search-available-numbers?connectionId=$CONNECTION_ID&areaCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "areaCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callScaler/latest/actions/search-available-numbers?${params}`, {
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
| `areaCode` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capabilities": {
        "mms": true,
        "sms": true,
        "voice": true
      },
      "friendly_name": "Ava Chen",
      "iso_country": "string",
      "number_type": "string",
      "phone_number": "string",
      "region": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capabilities.mms` | boolean | Whether MMS is supported. |
| `capabilities.sms` | boolean | Whether SMS is supported. |
| `capabilities.voice` | boolean | Whether voice is supported. |
| `friendly_name` | string | Formatted display name for the available number. |
| `iso_country` | string | ISO country code for the available number. |
| `number_type` | string | Available number type. |
| `phone_number` | string | Available phone number. |
| `region` | string | Region for the available number. |

## Native endpoint

Through the native CallScaler API, this operation is `POST /numbers/search` (base URL `https://callscaler.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-available-numbers.md) for the provider-specific parameters and requirements.

