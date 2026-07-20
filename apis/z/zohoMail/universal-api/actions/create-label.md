# Zoho Mail: Create Label

Creates a new label in Zoho Mail.

```
POST https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/create-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/create-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "3048445000000008002",
  "displayName": "CodexStageLabel"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/create-label', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "3048445000000008002",
    "displayName": "CodexStageLabel"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Account identifier returned by List Accounts. Example: `3048445000000008002`. |
| `displayName` | string | yes | Label name to create. Example: `CodexStageLabel`. |
| `color` | string | no | Optional label color as a hexadecimal value. Default: `#ffd700`. Example: `#ffd700`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "displayName": "Ava Chen",
      "labelId": "string",
      "sequence": 1,
      "tagId": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Label color |
| `displayName` | string | Label display name |
| `labelId` | string | Label identifier |
| `sequence` | number | Label sequence |
| `tagId` | string | Tag identifier |
| `uri` | string | Label API URI |

## Native endpoint

Through the native Zoho Mail API, this operation is `POST /accounts/:accountId/labels` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-label.md) for the provider-specific parameters and requirements.

