# HirePOS: Get Package

Finds a package in HirePOS by package code.

```
GET https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/get-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HirePOS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/get-package?connectionId=$CONNECTION_ID&packageCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packageCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hirePOS/latest/actions/get-package?${params}`, {
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
| `packageCode` | string | yes | Find a package by its exact HirePOS package code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "packageCode": "string",
      "packageDescription": "string",
      "packageItems": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | HirePOS identifier for the package. |
| `packageCode` | string | Exact package code used to retrieve the package. |
| `packageDescription` | string | Description of the package in HirePOS. |
| `packageItems` | array<object> | Package component items returned by HirePOS. |

## Native endpoint

Through the native HirePOS API, this operation is `GET /Packages` (base URL `https://api.hirepos.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-package.md) for the provider-specific parameters and requirements.

