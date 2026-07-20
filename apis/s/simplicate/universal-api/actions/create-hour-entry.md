# Simplicate: Create Hour Entry



```
POST https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/create-hour-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplicate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/create-hour-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/create-hour-entry', {
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
| `employeeId` | string | no | Employee identifier. |
| `hours` | string | no | Number of hours. |
| `note` | string | no | Hour entry note. |
| `projectId` | string | no | Project identifier. |
| `projectserviceId` | string | no | Project service identifier. |
| `source` | string | no | Hours source. |
| `startDate` | string | no | Entry start date in YYYY-MM-DD format. |
| `typeId` | string | no | Hour type identifier. |

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

Through the native Simplicate API, this operation is `POST /hours/hours` (base URL `https://{{credentials.subdomain}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-hour-entry.md) for the provider-specific parameters and requirements.

