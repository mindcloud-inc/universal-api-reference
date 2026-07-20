# fynk: Get Document Comment

Retrieves a document comment from fynk.

```
GET https://connect.mindcloud.co/v1/universal/fynk/latest/actions/get-document-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fynk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fynk/latest/actions/get-document-comment?connectionId=$CONNECTION_ID&comment=11111111-1111-1111-1111-111111111111&document=25c718b2-be8b-44e7-858f-3152e7380022" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "comment": "11111111-1111-1111-1111-111111111111",
  "document": "25c718b2-be8b-44e7-858f-3152e7380022"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fynk/latest/actions/get-document-comment?${params}`, {
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
| `comment` | string | yes | Comment UUID. Default: `11111111-1111-1111-1111-111111111111`. |
| `document` | string | yes | Document UUID. Default: `25c718b2-be8b-44e7-858f-3152e7380022`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native fynk API, this operation is `GET /documents/:document/comments/:comment` (base URL `https://app.fynk.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-comment.md) for the provider-specific parameters and requirements.

