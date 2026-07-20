# Flokzu: Operations



```
GET https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/operations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flokzu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/operations?connectionId=$CONNECTION_ID&oper=string&elem_1=string&elem_2=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "oper": "string",
  "elem_1": "string",
  "elem_2": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/operations?${params}`, {
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
| `oper` | string | yes | Operation code from Flokzu docs: sum, concat, or contains. |
| `elem_1` | string | yes | First input element for the selected operation. |
| `elem_2` | string | yes | Second input element for the selected operation. |
| `elem_N` | string | no | Optional additional input element for the selected operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | number | Result returned by the Flokzu Operations endpoint for the selected operation and inputs. |

## Native endpoint

Through the native Flokzu API, this operation is `POST /commons/MATH/operations` (base URL `https://app.flokzu.com/flokzuopenapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/operations.md) for the provider-specific parameters and requirements.

