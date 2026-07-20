# BSC Designer: Get Document Info



```
GET https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-document-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-document-info?connectionId=$CONNECTION_ID&idOrAlias=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrAlias": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-document-info?${params}`, {
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
| `idOrAlias` | string | yes | Document ID or alias. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "description": "string",
      "guid": "string",
      "icon": "string",
      "id": 1,
      "items": [
        {}
      ],
      "name": "Ava Chen",
      "ownerId": 1,
      "sharedForPublic": true,
      "sharedForRegRW": true,
      "treeGroupId": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string | Document alias. |
| `description` | string | Document description. |
| `guid` | string | Document GUID when available. |
| `icon` | string | Document icon path. |
| `id` | number | Document ID. |
| `items` | array<object> | Child tree items. |
| `name` | string | Document name. |
| `ownerId` | number | Owner user ID. |
| `sharedForPublic` | boolean | Whether the document is public. |
| `sharedForRegRW` | boolean | Whether the document is shared for registered read/write access. |
| `treeGroupId` | number | Parent tree group ID. |
| `type` | string | Document item type returned by BSC Designer. |

## Native endpoint

Through the native BSC Designer API, this operation is `GET /rest/api/documents/list/:idOrAlias` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-info.md) for the provider-specific parameters and requirements.

