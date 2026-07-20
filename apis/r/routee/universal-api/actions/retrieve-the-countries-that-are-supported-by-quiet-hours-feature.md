# Routee: Retrieve the countries that are supported by Quiet Hours feature

Retrieves the countries that are supported by quiet hours feature from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-the-countries-that-are-supported-by-quiet-hours-feature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-the-countries-that-are-supported-by-quiet-hours-feature?connectionId=$CONNECTION_ID&language=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "language": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-the-countries-that-are-supported-by-quiet-hours-feature?${params}`, {
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
| `language` | string | yes | The language code is ISO 639-1 format (el, en) that will be used to translate the country names. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "isoA3Code": "string",
      "localeName": "Ava Chen",
      "name": "Ava Chen",
      "supported": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `isoA3Code` | string |  |
| `localeName` | string |  |
| `name` | string |  |
| `supported` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /sms/quietHours/countries/:language` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-the-countries-that-are-supported-by-quiet-hours-feature.md) for the provider-specific parameters and requirements.

