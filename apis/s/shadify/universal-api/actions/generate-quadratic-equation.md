# Shadify: Generate Quadratic Equation

Retrieves a random quadratic equation from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-quadratic-equation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-quadratic-equation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-quadratic-equation?${params}`, {
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
| `minA` | number | no | Optional minimum value for coefficient A. Default is 1. Default: `1`. |
| `maxA` | number | no | Optional maximum value for coefficient A. Default is 20. Default: `20`. |
| `minB` | number | no | Optional minimum value for coefficient B. Default is 1. Default: `1`. |
| `maxB` | number | no | Optional maximum value for coefficient B. Default is 40. Default: `40`. |
| `minC` | number | no | Optional minimum value for coefficient C. Default is 1. Default: `1`. |
| `maxC` | number | no | Optional maximum value for coefficient C. Default is 20. Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "a": 1,
      "b": 1,
      "c": 1,
      "discriminant": 1,
      "equation": "string",
      "x1": "string",
      "x2": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `a` | number | Coefficient a. |
| `b` | number | Coefficient b. |
| `c` | number | Coefficient c. |
| `discriminant` | number | Discriminant value. |
| `equation` | string | Quadratic equation text. |
| `x1` | string | First root. |
| `x2` | string | Second root. |

## Native endpoint

Through the native Shadify API, this operation is `GET /math/quad` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-quadratic-equation.md) for the provider-specific parameters and requirements.

