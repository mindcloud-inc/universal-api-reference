# Mighty Tix: Update Session

Updates an existing session in Mighty Tix.

```
PUT https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/update-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Tix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/update-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.input": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mightyTix/latest/actions/update-session', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.input": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input` | object | yes | UpdateOneSessionInput object from the Mighty Tix Admin GraphQL docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "2026-05-07T12:00:00.000Z",
      "eventId": "string",
      "id": "string",
      "offsale": "2026-05-07T12:00:00.000Z",
      "onsale": "2026-05-07T12:00:00.000Z",
      "start": "2026-05-07T12:00:00.000Z",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | date |  |
| `eventId` | string |  |
| `id` | string |  |
| `offsale` | date |  |
| `onsale` | date |  |
| `start` | date |  |
| `updated` | date |  |

## Native endpoint

Through the native Mighty Tix API, this operation is `POST admin-api/graphql` (base URL `https://mindcloudmttix260403.mightytix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-session.md) for the provider-specific parameters and requirements.

