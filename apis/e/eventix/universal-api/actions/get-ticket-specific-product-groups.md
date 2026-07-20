# Eventix: Get all ProductGroups for this Ticket Type

Retrieves product groups for an Eventix ticket type.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-ticket-specific-product-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-ticket-specific-product-groups?connectionId=$CONNECTION_ID&guid=ticket-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "ticket-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-ticket-specific-product-groups?${params}`, {
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
| `guid` | string | yes | The guid of the Ticket Type. Example: `ticket-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "denominator": 1,
      "description": "string",
      "guid": "string",
      "max_bound": 1,
      "members": [
        "string"
      ],
      "min_bound": 1,
      "name": "Ava Chen",
      "numerator": 1,
      "preceded_by": "string",
      "ticket_id": "string",
      "uniqueness": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `denominator` | number |  |
| `description` | string |  |
| `guid` | string |  |
| `max_bound` | number |  |
| `members` | array<string> |  |
| `min_bound` | number |  |
| `name` | string |  |
| `numerator` | number |  |
| `preceded_by` | string |  |
| `ticket_id` | string |  |
| `uniqueness` | number |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/ticket/:guid/groups` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ticket-specific-product-groups.md) for the provider-specific parameters and requirements.

