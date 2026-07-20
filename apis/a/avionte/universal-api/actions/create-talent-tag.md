# Avionte: Create Talent Tag



```
POST https://connect.mindcloud.co/v1/universal/avionte/latest/actions/create-talent-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avionte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avionte/latest/actions/create-talent-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tag": "string",
  "talentId": "string",
  "bodyTalentId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avionte/latest/actions/create-talent-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tag": "string",
    "talentId": "string",
    "bodyTalentId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tag` | string | yes |  |
| `talentId` | string | yes |  |
| `detail` | string | no |  |
| `expirationDate` | date | no |  |
| `bodyTalentId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avionte API returns.

## Native endpoint

Through the native Avionte API, this operation is `POST front-office/v1/talent/:talentId/talenttag` (base URL `https://api.avionte.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-talent-tag.md) for the provider-specific parameters and requirements.

