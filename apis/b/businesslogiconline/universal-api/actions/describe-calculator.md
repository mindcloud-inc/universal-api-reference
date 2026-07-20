# Businesslogic.online: Describe Calculator

Retrieves calculator input and output schemas from Businesslogic.online.

```
GET https://connect.mindcloud.co/v1/universal/businesslogiconline/latest/actions/describe-calculator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Businesslogic.online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/businesslogiconline/latest/actions/describe-calculator?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/businesslogiconline/latest/actions/describe-calculator?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "available_data": {},
      "expected_input": {},
      "expected_output": {},
      "name": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available_data` | object | Provider-supplied object describing any extra available calculator data. |
| `expected_input` | object | JSON Schema describing the calculator input payload. |
| `expected_output` | object | JSON Schema describing the calculator output payload. |
| `name` | string | Calculator name returned by the describe endpoint. |
| `version` | string | Calculator version returned by the describe endpoint. |

## Native endpoint

Through the native Businesslogic.online API, this operation is `GET /describe` (base URL `https://api.businesslogic.online`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-calculator.md) for the provider-specific parameters and requirements.

