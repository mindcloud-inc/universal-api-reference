# JetAPI: Lookup Phone Operator

Finds a phone operator in JetAPI by number.

```
GET https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/lookup-phone-operator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JetAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/lookup-phone-operator?connectionId=$CONNECTION_ID&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/lookup-phone-operator?${params}`, {
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
| `phone` | string | yes | Phone number in international format. Special characters are allowed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formattedPhone": "string",
      "meta": {},
      "operator": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formattedPhone` | string |  |
| `meta` | object |  |
| `operator` | object |  |

## Native endpoint

Through the native JetAPI API, this operation is `GET /api/v1/operators/search` (base URL `https://api.jetapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-phone-operator.md) for the provider-specific parameters and requirements.

