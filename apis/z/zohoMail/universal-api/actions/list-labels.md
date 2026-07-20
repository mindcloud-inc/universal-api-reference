# Zoho Mail: List Labels

Retrieves all labels from Zoho Mail.

```
GET https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/list-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/list-labels?connectionId=$CONNECTION_ID&accountId=3048445000000008002" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "3048445000000008002"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/list-labels?${params}`, {
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
| `accountId` | string | yes | Account identifier returned by List Accounts. Example: `3048445000000008002`. |

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

Through the native Zoho Mail API, this operation is `GET /accounts/:accountId/labels` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-labels.md) for the provider-specific parameters and requirements.

