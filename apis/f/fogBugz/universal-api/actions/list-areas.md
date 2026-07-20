# FogBugz: List Areas

Retrieves areas from FogBugz.

```
GET https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-areas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FogBugz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-areas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-areas?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fWrite` | boolean | no | Set to true to include only areas you can modify. |
| `ixProject` | number | no | Limit results to areas in a specific project. |
| `ixArea` | number | no | Include a specific area even if it is deleted. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cDoc": 1,
      "ixArea": 1,
      "ixPersonOwner": 1,
      "ixProject": 1,
      "nType": 1,
      "sArea": "string",
      "sPersonOwner": "string",
      "sProject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cDoc` | number | Document count. |
| `ixArea` | number | Area ID. |
| `ixPersonOwner` | number | Owner person ID. |
| `ixProject` | number | Project ID. |
| `nType` | number | Area type code. |
| `sArea` | string | Area name. |
| `sPersonOwner` | string | Owner name. |
| `sProject` | string | Project name. |

## Native endpoint

Through the native FogBugz API, this operation is `POST /listAreas` (base URL `{{credentials.siteUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-areas.md) for the provider-specific parameters and requirements.

