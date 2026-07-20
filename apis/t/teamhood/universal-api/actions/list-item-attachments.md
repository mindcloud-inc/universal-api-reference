# Teamhood: List Item Attachments

Retrieves attachments for a Teamhood item.

```
GET https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-item-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamhood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-item-attachments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-item-attachments?${params}`, {
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
| `itemId` | string | no | The Teamhood item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> | Attachments on the specified Teamhood item. |

## Native endpoint

Through the native Teamhood API, this operation is `GET /items/:itemId/attachments` (base URL `https://api-mindcloud1.teamhood.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-item-attachments.md) for the provider-specific parameters and requirements.

