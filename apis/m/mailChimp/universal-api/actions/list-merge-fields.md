# Mailchimp: List Merge Fields

Retrieves merge fields from a Mailchimp audience.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-merge-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-merge-fields?connectionId=$CONNECTION_ID&limit=25&offset=0&list_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "list_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-merge-fields?${params}`, {
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
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `list_id` | string | yes | The unique ID for the Mailchimp audience. |
| `required` | boolean | no |  |
| `type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        [
          {}
        ]
      ],
      "listId": "string",
      "mergeFields": [
        [
          {}
        ]
      ],
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links[]` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |
| `links[].schema` | string |  |
| `links[].targetSchema` | string |  |
| `listId` | string |  |
| `mergeFields[]` | array<object> |  |
| `mergeFields[].defaultValue` | string |  |
| `mergeFields[].displayOrder` | number |  |
| `mergeFields[].helpText` | string |  |
| `mergeFields[].links[]` | array<object> |  |
| `mergeFields[].links[].href` | string |  |
| `mergeFields[].links[].method` | string |  |
| `mergeFields[].links[].rel` | string |  |
| `mergeFields[].links[].targetSchema` | string |  |
| `mergeFields[].listId` | string |  |
| `mergeFields[].mergeId` | number |  |
| `mergeFields[].name` | string |  |
| `mergeFields[].options` | object |  |
| `mergeFields[].options.defaultCountry` | number |  |
| `mergeFields[].public` | boolean |  |
| `mergeFields[].required` | boolean |  |
| `mergeFields[].tag` | string |  |
| `mergeFields[].type` | string |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `GET lists/:list_id/merge-fields` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-merge-fields.md) for the provider-specific parameters and requirements.

