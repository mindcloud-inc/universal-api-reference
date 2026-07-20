# Print.one Postcards: Delete Template

Deletes an existing template from Print.one Postcards.

```
DELETE https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/delete-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/delete-template?${params}`, {
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
| `id` | string | yes | Template ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": 1,
      "format": "string",
      "id": "string",
      "labels": [
        "string"
      ],
      "mergeVariables": [
        "string"
      ],
      "name": "Ava Chen",
      "options": {
        "doubleSided": true
      },
      "overlay": "string",
      "pages": [
        {
          "content": "string",
          "friendlyName": "Ava Chen",
          "orderingKey": 1
        }
      ],
      "thumbnail": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | number |  |
| `format` | string |  |
| `id` | string |  |
| `labels` | array<string> |  |
| `mergeVariables` | array<string> |  |
| `name` | string |  |
| `options` | object |  |
| `options.doubleSided` | boolean |  |
| `overlay` | string |  |
| `pages` | array<object> |  |
| `pages[].content` | string |  |
| `pages[].friendlyName` | string |  |
| `pages[].orderingKey` | number |  |
| `thumbnail` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `DELETE /v2/templates/[:id]` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

