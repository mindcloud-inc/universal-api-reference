# Nautical: List Email Templates

Retrieves a list of email templates from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-email-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-email-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-email-templates?${params}`, {
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
      "data": {
        "emailTemplates": {
          "edges": [
            {
              "node": {
                "createdAt": "ava@example.com",
                "id": "ava@example.com",
                "senderEmailAddress": "ava@example.com",
                "subject": "ava@example.com",
                "title": "ava@example.com"
              }
            }
          ],
          "pageInfo": {
            "endCursor": "ava@example.com",
            "hasNextPage": true
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.emailTemplates.edges[].node.createdAt` | string |  |
| `data.emailTemplates.edges[].node.id` | string |  |
| `data.emailTemplates.edges[].node.senderEmailAddress` | string |  |
| `data.emailTemplates.edges[].node.subject` | string |  |
| `data.emailTemplates.edges[].node.title` | string |  |
| `data.emailTemplates.pageInfo.endCursor` | string |  |
| `data.emailTemplates.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-templates.md) for the provider-specific parameters and requirements.

