# Syntage: Get Tax Compliance Check

Retrieves a tax compliance check from Syntage.

```
GET https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-tax-compliance-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syntage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-tax-compliance-check?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syntage/latest/actions/get-tax-compliance-check?${params}`, {
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
| `id` | string | yes | The tax compliance check identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@id": "string",
      "@type": "string",
      "checkedAt": "string",
      "createdAt": "string",
      "file": {},
      "id": "string",
      "internalIdentifier": "string",
      "result": "string",
      "taxpayer": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@id` | string |  |
| `@type` | string |  |
| `checkedAt` | string |  |
| `createdAt` | string |  |
| `file` | object |  |
| `id` | string |  |
| `internalIdentifier` | string |  |
| `result` | string |  |
| `taxpayer` | object |  |

## Native endpoint

Through the native Syntage API, this operation is `GET /tax-compliance-checks/:id` (base URL `https://api.sandbox.syntage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tax-compliance-check.md) for the provider-specific parameters and requirements.

