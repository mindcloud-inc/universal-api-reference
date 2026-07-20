# Maildroppa: Update Segment



```
PUT https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/update-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/update-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriberSegmentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/update-segment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriberSegmentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expression` | object | no | Filter expression defining the segment criteria. |
| `name` | string | no | Display name for the segment. |
| `subscriberSegmentId` | string | yes | Unique identifier of the segment to update. |

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

Through the native Maildroppa API, this operation is `PUT /subscriber/segment/{subscriberSegmentId}` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-segment.md) for the provider-specific parameters and requirements.

