# Jodoo: Get Approval Comments



```
GET https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-approval-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-approval-comments?connectionId=$CONNECTION_ID&appId=69c4042cce7f5503d03455c1&entryId=63e7f8b6b8c3070007092dae&dataId=69c4170644fbc638af9a2d4f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "69c4042cce7f5503d03455c1",
  "entryId": "63e7f8b6b8c3070007092dae",
  "dataId": "69c4170644fbc638af9a2d4f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-approval-comments?${params}`, {
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
| `appId` | string | yes | Jodoo app ID that owns the workflow form. Example: `69c4042cce7f5503d03455c1`. |
| `entryId` | string | yes | Jodoo workflow form ID. Example: `63e7f8b6b8c3070007092dae`. |
| `dataId` | string | yes | Workflow form record ID. Example: `69c4170644fbc638af9a2d4f`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of approval comments to skip. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approveCommentList": [
        {
          "comment": "string",
          "flowAction": "string",
          "flowNodeName": "Ava Chen",
          "operator": {
            "name": "Ava Chen",
            "status": 1,
            "username": "Ava Chen"
          },
          "signatureUrl": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approveCommentList[].comment` | string |  |
| `approveCommentList[].flowAction` | string |  |
| `approveCommentList[].flowNodeName` | string |  |
| `approveCommentList[].operator.name` | string |  |
| `approveCommentList[].operator.status` | number |  |
| `approveCommentList[].operator.username` | string |  |
| `approveCommentList[].signatureUrl` | string |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST https://api.jodoo.com/api/v1/app/:app_id/entry/:entry_id/data/:data_id/approval_comments` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-approval-comments.md) for the provider-specific parameters and requirements.

