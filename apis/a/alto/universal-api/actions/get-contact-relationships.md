# Alto: Get Contact Relationships

Retrieves contact relationships from Alto by contact ID.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-contact-relationships
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-contact-relationships?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-contact-relationships?${params}`, {
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
| `contactId` | string | yes | Unique Alto contact identifier. |
| `relationshipType` | string | no | Relationship type filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1,
      "relationships": [
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
| `contactId` | number |  |
| `relationships` | array<object> |  |

## Native endpoint

Through the native Alto API, this operation is `GET /contacts/:contactId/relationship` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-relationships.md) for the provider-specific parameters and requirements.

