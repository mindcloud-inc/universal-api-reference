# Ascora: List Supplies

Retrieves supplies from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-supplies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-supplies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-supplies?${params}`, {
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
| `categoryOneId` | string | no | Filter by category one ID. |
| `categoryTwoId` | string | no | Filter by category two ID. |
| `favouriteOnly` | boolean | no | Restrict to favourite supplies only. |
| `filterText` | string | no | Search across part number, supplier part number, description, annotation, and category one name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ],
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Matching supply records. |
| `success` | boolean | Whether Ascora returned the supplies search successfully. |
| `totalPages` | number | Total result pages returned by Ascora. |
| `totalRecords` | number | Total matching supplies. |

## Native endpoint

Through the native Ascora API, this operation is `GET /Inventory/Supplies` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supplies.md) for the provider-specific parameters and requirements.

