# Documo: Validate Fax Number

Validates a fax number in Documo.

```
GET https://connect.mindcloud.co/v1/universal/documo/latest/actions/validate-fax-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documo/latest/actions/validate-fax-number?connectionId=$CONNECTION_ID&number=string&country=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "string",
  "country": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documo/latest/actions/validate-fax-number?${params}`, {
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
| `number` | string | yes | The fax number to validate. |
| `country` | string | yes | The alpha-2 country code for the number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isValid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isValid` | boolean |  |

## Native endpoint

Through the native Documo API, this operation is `GET /v1/numbers/validate` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-fax-number.md) for the provider-specific parameters and requirements.

