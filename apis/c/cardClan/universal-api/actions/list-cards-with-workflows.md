# CardClan: List Cards With Workflows

Retrieves CardClan cards with active integration workflows.

```
GET https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/list-cards-with-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CardClan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/list-cards-with-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cardClan/latest/actions/list-cards-with-workflows?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Workflow-enabled cards visible to the authenticated user. |
| `message` | string | Workflow-card lookup result message. |

## Native endpoint

Through the native CardClan API, this operation is `GET /integration/workflow-cards` (base URL `https://app.cardclan.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cards-with-workflows.md) for the provider-specific parameters and requirements.

