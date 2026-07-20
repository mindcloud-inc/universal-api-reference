# Wisewand: Create and run a categorypages

Creates and runs a category page in Wisewand.

```
POST https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/create-and-run-a-categorypages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/create-and-run-a-categorypages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "MindCloud Wisewand validator test subject"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/create-and-run-a-categorypages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "MindCloud Wisewand validator test subject"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | The subject of the category page. Default: `MindCloud Wisewand validator test subject`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Wisewand API, this operation is `POST /v1/categorypages/` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-and-run-a-categorypages.md) for the provider-specific parameters and requirements.

