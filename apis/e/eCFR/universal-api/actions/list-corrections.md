# eCFR: List Corrections

Retrieves a list of corrections from eCFR.

```
GET https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/list-corrections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eCFR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/list-corrections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCFR/latest/actions/list-corrections?${params}`, {
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
| `title` | number | no | Optional CFR title number to filter corrections, such as 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ecfr_corrections": [
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
| `ecfr_corrections` | array<object> | eCFR correction records. |

## Native endpoint

Through the native eCFR API, this operation is `GET /api/admin/v1/corrections.json` (base URL `https://www.ecfr.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-corrections.md) for the provider-specific parameters and requirements.

