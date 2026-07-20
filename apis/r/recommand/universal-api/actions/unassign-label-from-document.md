# Recommand: Unassign Label from Document

Removes a label from a Recommand document.

```
DELETE https://connect.mindcloud.co/v1/universal/recommand/latest/actions/unassign-label-from-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/unassign-label-from-document?connectionId=$CONNECTION_ID&documentid=string&labelid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentid": "string",
  "labelid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/unassign-label-from-document?${params}`, {
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
| `documentid` | string | yes | documentId parameter. |
| `labelid` | string | yes | labelId parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `DELETE /api/v1/documents/:documentId/labels/:labelId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unassign-label-from-document.md) for the provider-specific parameters and requirements.

