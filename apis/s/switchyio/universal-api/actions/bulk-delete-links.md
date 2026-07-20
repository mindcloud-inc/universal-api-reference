# Switchy.io: Bulk Delete Links

Deletes existing links from Switchy.io by domain and IDs.

```
DELETE https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/bulk-delete-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Switchy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/bulk-delete-links?connectionId=$CONNECTION_ID&domain=string&idsCsv=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "idsCsv": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/bulk-delete-links?${params}`, {
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
| `domain` | string | yes |  |
| `idsCsv` | string | yes | Comma-separated link ids within the selected domain |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affected_rows": 1,
      "returning": [
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
| `affected_rows` | number |  |
| `returning` | array<object> |  |

## Native endpoint

Through the native Switchy.io API, this operation is `POST /v1/graphql` (base URL `https://graphql.switchy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-delete-links.md) for the provider-specific parameters and requirements.

