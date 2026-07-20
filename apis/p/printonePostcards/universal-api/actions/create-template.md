# Print.one Postcards: Create Template

Creates a new template in Print.one Postcards.

```
POST https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "format": "string",
  "labels[]": [
    "string"
  ],
  "pages[]": [
    {}
  ],
  "overlay": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "format": "string",
    "labels[]": ["string"],
    "pages[]": [{}],
    "overlay": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Template name. |
| `format` | string | yes | Template format. |
| `labels[]` | array<string> | yes | Labels attached to this template. |
| `pages[]` | array<object> | yes | Template pages as an array of objects with content. |
| `overlay` | string | yes | Postal overlay. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `options` | object | no | Template options. |

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
| `labels[]` | string |  |
| `mergeVariables[]` | string |  |
| `name` | string |  |
| `options.doubleSided` | boolean |  |
| `overlay` | string |  |
| `pages[].content` | string |  |
| `pages[].friendlyName` | string |  |
| `pages[].orderingKey` | number |  |
| `updatedAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `POST /v2/templates` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

