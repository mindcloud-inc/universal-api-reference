# Shadify: Generate Schulte Table

Retrieves a random Schulte table from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-schulte-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-schulte-table?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-schulte-table?${params}`, {
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
| `size` | number | no | Optional table size from 1 to 15. Default is 5. Default: `5`. |
| `mode` | list | no | Optional number or alphabet mode. Default is number. One of: `0`, `1`. Default: `number`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "grid": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `grid` | array<array> | Generated Schulte table grid. |

## Native endpoint

Through the native Shadify API, this operation is `GET /schulte/generator` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-schulte-table.md) for the provider-specific parameters and requirements.

