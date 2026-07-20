# SMS Connexion: Validate Number

Validates a phone number in SMS Connexion.

```
GET https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/validate-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/validate-number?connectionId=$CONNECTION_ID&phoneNumber=%2B4915123772462" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "+4915123772462"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/validate-number?${params}`, {
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
| `phoneNumber` | string | yes | Phone number in E.164 format, e.g. +4915123772462. Example: `+4915123772462`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countryIso": "string",
      "networkOperator": "string",
      "phoneNumber": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryIso` | string |  |
| `networkOperator` | string |  |
| `phoneNumber` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `GET /numbers/validate/:phoneNumber` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-number.md) for the provider-specific parameters and requirements.

