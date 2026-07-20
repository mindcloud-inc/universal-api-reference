# ProductLift: Get Portal



```
GET https://connect.mindcloud.co/v1/universal/productLift/latest/actions/get-portal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProductLift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productLift/latest/actions/get-portal?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productLift/latest/actions/get-portal?${params}`, {
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
      "editorType": "string",
      "guid": "string",
      "inviteMessage": "string",
      "jiraDomainUrl": "https://example.com",
      "jiraEnabled": true,
      "localization": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `editorType` | string | Portal editor type. |
| `guid` | string | Portal GUID. |
| `inviteMessage` | string | Portal invite message. |
| `jiraDomainUrl` | string | Configured Jira domain URL when present. |
| `jiraEnabled` | boolean | Whether Jira integration is enabled. |
| `localization` | string | Portal locale code. |
| `title` | string | Portal title. |

## Native endpoint

Through the native ProductLift API, this operation is `GET /portal` (base URL `https://mindcloud.productlift.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-portal.md) for the provider-specific parameters and requirements.

