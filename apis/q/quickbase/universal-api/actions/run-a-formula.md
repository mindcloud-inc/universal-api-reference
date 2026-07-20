# Quickbase: Run a Formula

Evaluates a Quickbase formula and returns the result.

```
GET https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/run-a-formula
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/run-a-formula?connectionId=$CONNECTION_ID&from=string&formula=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string",
  "formula": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/run-a-formula?${params}`, {
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
| `from` | string | yes | The Quickbase table identifier. |
| `formula` | string | yes | The Quickbase formula to run. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `rid` | number | no | Optional record ID for formulas that require record context. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | The formula result returned by Quickbase. |

## Native endpoint

Through the native Quickbase API, this operation is `POST v1/formula/run` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-a-formula.md) for the provider-specific parameters and requirements.

