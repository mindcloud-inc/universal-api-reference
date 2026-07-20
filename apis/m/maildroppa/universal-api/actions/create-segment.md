# Maildroppa: Create Segment



```
POST https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/create-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/create-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/create-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expression` | string | no | Filter expression defining the segment criteria. |
| `name` | string | no | Display name for the segment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expression": {
        "filterGroups": [
          {
            "elements": [
              {}
            ]
          }
        ],
        "operator": "string"
      },
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expression.filterGroups[].elements` | array<object> | List of filter elements in this group. |
| `expression.operator` | string | Logical operator that applies between filter groups. |
| `id` | string | Unique identifier of the segment. |
| `name` | string | Display name for the segment. |

## Native endpoint

Through the native Maildroppa API, this operation is `POST /subscriber/segment` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-segment.md) for the provider-specific parameters and requirements.

