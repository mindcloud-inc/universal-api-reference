# Environmental Protection Agency: List Parameters By Class

Retrieves parameters for a class from EPA AQS.

```
GET https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-parameters-by-class
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Environmental Protection Agency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-parameters-by-class?connectionId=$CONNECTION_ID&pc=CRITERIA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pc": "CRITERIA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/environmentalProtectionAgency/latest/actions/list-parameters-by-class?${params}`, {
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
| `pc` | string | yes | AQS parameter class name. Use ALL for every parameter class or a class returned by List Parameter Classes. Example: `CRITERIA`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "value_represented": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | EPA AQS code value. |
| `value_represented` | string | Meaning represented by the EPA AQS code. |

## Native endpoint

Through the native Environmental Protection Agency API, this operation is `GET /list/parametersByClass` (base URL `https://aqs.epa.gov/data/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-parameters-by-class.md) for the provider-specific parameters and requirements.

