# Sendblue: Lookup Phone Number

Determines whether a phone number supports iMessage or SMS.

```
GET https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/lookup-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/lookup-phone-number?connectionId=$CONNECTION_ID&number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/lookup-phone-number?${params}`, {
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
| `number` | string | yes | The number to evaluate in E.164 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "number": "string",
      "service": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `number` | string |  |
| `service` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `GET /api/evaluate-service` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-phone-number.md) for the provider-specific parameters and requirements.

