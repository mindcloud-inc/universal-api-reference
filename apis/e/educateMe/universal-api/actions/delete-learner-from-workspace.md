# EducateMe: Delete Learner from Workspace

Deletes an existing learner from EducateMe.

```
DELETE https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/delete-learner-from-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/delete-learner-from-workspace?connectionId=$CONNECTION_ID&email=codex.learner.two.20260331%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "codex.learner.two.20260331@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/delete-learner-from-workspace?${params}`, {
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
| `email` | string | yes | Learner email. Example: `codex.learner.two.20260331@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the learner was deleted from the workspace successfully. |

## Native endpoint

Through the native EducateMe API, this operation is `DELETE /students/:email` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-learner-from-workspace.md) for the provider-specific parameters and requirements.

