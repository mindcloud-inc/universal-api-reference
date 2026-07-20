# Wisewand: Get the cost of creating one updateposts

Retrieves update post creation cost from Wisewand.

```
POST https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-the-cost-of-creating-one-updateposts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wisewand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-the-cost-of-creating-one-updateposts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "MindCloud Wisewand validator test subject"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wisewand/latest/actions/get-the-cost-of-creating-one-updateposts', {
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
| `subject` | string | yes | The subject of the article. It can also contains source URLs. Default: `MindCloud Wisewand validator test subject`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": 1,
      "credits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | number |  |
| `credits` | number |  |

## Native endpoint

Through the native Wisewand API, this operation is `POST /v1/updateposts/cost` (base URL `https://api.wisewand.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-the-cost-of-creating-one-updateposts.md) for the provider-specific parameters and requirements.

