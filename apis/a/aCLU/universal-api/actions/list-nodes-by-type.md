# ACLU: List Nodes By Type

Retrieves Torture Database nodes by content type.

```
GET https://connect.mindcloud.co/v1/universal/aCLU/latest/actions/list-nodes-by-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ACLU `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aCLU/latest/actions/list-nodes-by-type?connectionId=$CONNECTION_ID&name=document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "document"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aCLU/latest/actions/list-nodes-by-type?${params}`, {
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
| `page` | number | no | Zero-based page number. The docs say page=0 by default. Default: `0`. |
| `name` | string | yes | Use one documented value exactly: agency, Authors/Recipients, Document Types, Techniques, detainee, document, incident, location, official, or source. Default: `document`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nid": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nid` | number |  |
| `title` | string |  |

## Native endpoint

Through the native ACLU API, this operation is `GET /getnode/retrieve.json` (base URL `https://www.thetorturedatabase.org/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-nodes-by-type.md) for the provider-specific parameters and requirements.

